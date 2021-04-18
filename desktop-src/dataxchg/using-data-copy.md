---
title: Verwenden der Datenkopie
description: Dieses Thema enthält ein Beispiel, das veranschaulicht, wie Informationen zwischen zwei Anwendungen gesendet werden.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Windows-Benutzeroberfläche, Datenkopie
- Kopieren von Daten, Beispiele
- Kopieren von Daten, WM_COPYDATA Nachricht
- WM_COPYDATA Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e44c4abb9aba68d4db1544f5c7d52220cdc681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340273"
---
# <a name="using-data-copy"></a>Verwenden der Datenkopie

Im folgenden Beispiel wird veranschaulicht, wie Informationen zwischen zwei Anwendungen mithilfe der ". [**\_ CopyData**](wm-copydata.md) "-Nachricht gesendet werden.

Die sendende Anwendung zeigt ein Dialogfeld für den Benutzer an, der bestimmte Informationen anfordert. Die Anwendung verpackt die Informationen in eine private Datenstruktur, enthält einen Zeiger auf die-Struktur in der [**copydatastruct**](/windows/win32/api/winuser/ns-winuser-copydatastruct) -Struktur und sendet die Informationen mithilfe der ". [**\_ CopyData**](wm-copydata.md) "-Nachricht an die empfangende Anwendung. Die empfangende Anwendung verfügt über ein verborgenes Fenster mit dem Klassennamen Disp32Class.


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



Die empfangende Anwendung verfügt über ein ausgeblendetes Fenster, das die Informationen von [**WM \_ CopyData**](wm-copydata.md) empfängt und für den Benutzer anzeigt.


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

[**FindWindow**](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 