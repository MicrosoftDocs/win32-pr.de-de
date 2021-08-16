---
description: Eine Möglichkeit, ein Gerätekontexthandle für einen Drucker abzurufen, besteht darin, ein Druckdialogfeld anzuzeigen und dem Benutzer die Auswahl eines Druckers zu ermöglichen.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Anzeigen eines Druckdialogfelds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113c9235e70712a4923ebdc3ad239f533160eb2f84f76ae729d7fadf203ca612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036828"
---
# <a name="displaying-a-print-dialog-box"></a>Anzeigen eines Druckdialogfelds

Eine Möglichkeit, ein Gerätekontexthandle für einen Drucker abzurufen, besteht darin, ein Druckdialogfeld anzuzeigen und dem Benutzer die Auswahl eines Druckers zu ermöglichen. Die [PrintDlg-Funktion](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (die das Dialogfeld anzeigt) verfügt über einen Parameter, der die Adresse einer [PRINTDLG-Struktur](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) darstellt. Die PRINTDLG-Struktur verfügt über mehrere Member, aber Sie können die meisten elemente auf ihre Standardwerte festlegen. Die beiden Elemente, die Sie festlegen müssen, sind **lStructSize** und **Flags.** Legen Sie **lStructSize** auf die Größe einer PRINTDLG-Variablen und **Flags** auf PD \_ RETURNDC fest. Das Festlegen von **Flags** auf PC \_ RETURNDC gibt an, dass die PrintDlg-Funktion das **hDC-Feld** mit einem Gerätekontexthandle für den vom Benutzer ausgewählten Drucker füllen soll.


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
