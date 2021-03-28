---
description: Eine Möglichkeit, ein Gerätekontext Handle für einen Drucker zu erhalten, besteht darin, ein Druck Dialogfeld anzuzeigen und dem Benutzer zu ermöglichen, einen Drucker auszuwählen.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Anzeigen eines Druck Dialogfelds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0d40365c36e3e554812ff137475ab7c6405e91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994278"
---
# <a name="displaying-a-print-dialog-box"></a>Anzeigen eines Druck Dialogfelds

Eine Möglichkeit, ein Gerätekontext Handle für einen Drucker zu erhalten, besteht darin, ein Druck Dialogfeld anzuzeigen und dem Benutzer zu ermöglichen, einen Drucker auszuwählen. Die [PRINTDLG](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion (die das Dialogfeld anzeigt) verfügt über einen Parameter, der die Adresse einer [PRINTDLG](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) -Struktur ist. Die PRINTDLG-Struktur verfügt über mehrere Member, aber Sie können die meisten dieser Elemente auf ihre Standardwerte festlegen. Die zwei Member, die Sie festlegen müssen, sind **lStructSize** und **Flags**. Legen Sie **lStructSize** auf die Größe einer PRINTDLG-Variablen fest, und legen Sie **Flags** auf PD \_ returndc fest. Das Festlegen von **Flags** auf \_ den PC returndc gibt an, dass die PrintDlg-Funktion das **hdc** -Feld mit einem Gerätekontext Handle für den vom Benutzer ausgewählten Drucker ausfüllen soll.


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



 

 
