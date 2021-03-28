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
# <a name="displaying-a-print-dialog-box"></a><span data-ttu-id="a1702-103">Anzeigen eines Druck Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="a1702-103">Displaying a Print Dialog Box</span></span>

<span data-ttu-id="a1702-104">Eine Möglichkeit, ein Gerätekontext Handle für einen Drucker zu erhalten, besteht darin, ein Druck Dialogfeld anzuzeigen und dem Benutzer zu ermöglichen, einen Drucker auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a1702-104">One way to get a device context handle for a printer is to display a print dialog box and allow the user to choose a printer.</span></span> <span data-ttu-id="a1702-105">Die [PRINTDLG](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion (die das Dialogfeld anzeigt) verfügt über einen Parameter, der die Adresse einer [PRINTDLG](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="a1702-105">The [PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function (which displays the dialog box) has one parameter that is the address of a [PRINTDLG](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) structure.</span></span> <span data-ttu-id="a1702-106">Die PRINTDLG-Struktur verfügt über mehrere Member, aber Sie können die meisten dieser Elemente auf ihre Standardwerte festlegen.</span><span class="sxs-lookup"><span data-stu-id="a1702-106">The PRINTDLG structure has several members, but you can leave most of them set to their default values.</span></span> <span data-ttu-id="a1702-107">Die zwei Member, die Sie festlegen müssen, sind **lStructSize** und **Flags**.</span><span class="sxs-lookup"><span data-stu-id="a1702-107">The two members you need to set are **lStructSize** and **Flags**.</span></span> <span data-ttu-id="a1702-108">Legen Sie **lStructSize** auf die Größe einer PRINTDLG-Variablen fest, und legen Sie **Flags** auf PD \_ returndc fest.</span><span class="sxs-lookup"><span data-stu-id="a1702-108">Set **lStructSize** to the size of a PRINTDLG variable, and set **Flags** to PD\_RETURNDC.</span></span> <span data-ttu-id="a1702-109">Das Festlegen von **Flags** auf \_ den PC returndc gibt an, dass die PrintDlg-Funktion das **hdc** -Feld mit einem Gerätekontext Handle für den vom Benutzer ausgewählten Drucker ausfüllen soll.</span><span class="sxs-lookup"><span data-stu-id="a1702-109">Setting **Flags** to PC\_RETURNDC specifies that you want the PrintDlg function to fill the **hDC** field with a device context handle for the printer chosen by the user.</span></span>


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



 

 
