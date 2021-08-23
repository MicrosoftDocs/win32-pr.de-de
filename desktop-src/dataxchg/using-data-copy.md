---
title: Verwenden von Datenkopiervorgang
description: Dieses Thema enthält ein Beispiel, das das Senden von Informationen zwischen zwei Anwendungen veranschaulicht.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Windows Benutzeroberfläche,Datenkopiervorgang
- Datenkopie, Beispiele
- Datenkopie,WM_COPYDATA Meldung
- WM_COPYDATA Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231a03a30c578590dabf04d740f917a791a86d0e868d3587ff0b63bf283866f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730555"
---
# <a name="using-data-copy"></a>Verwenden von Datenkopiervorgang

Im folgenden Beispiel wird veranschaulicht, wie Informationen zwischen zwei Anwendungen mithilfe der [**WM \_ COPYDATA-Nachricht**](wm-copydata.md) gesendet werden.

Die sendende Anwendung zeigt dem Benutzer ein Dialogfeld an, in dem bestimmte Informationen angefordert werden. Die Anwendung packt die Informationen in eine private Datenstruktur, enthält einen Zeiger auf die Struktur in der [**COPYDATASTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-copydatastruct) und sendet die Informationen mithilfe der [**WM \_ COPYDATA-Nachricht**](wm-copydata.md) an die empfangende Anwendung. Die empfangende Anwendung verfügt über ein ausgeblendetes Fenster mit dem Klassennamen Disp32Class.


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



Die empfangende Anwendung verfügt über ein ausgeblendetes Fenster, das die Informationen von [**WM \_ COPYDATA**](wm-copydata.md) empfängt und dem Benutzer anzeigt.


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Findwindow**](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 