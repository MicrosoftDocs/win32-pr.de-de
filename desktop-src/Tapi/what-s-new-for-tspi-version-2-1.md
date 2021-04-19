---
description: Beginnend mit TAPI 2,1 können die Benutzeroberflächen-DLLs des Telefoniedienstanbieters zum Verwalten und Anzeigen von Dialogfeldern verwendet werden. TAPI lädt die dll in den Prozess einer Anwendung, die eine beliebige Dienstanbieter Funktion aufruft, die ein Dialogfeld anzeigen kann.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Neuerungen bei TSPI Version 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349494"
---
# <a name="whats-new-for-tspi-version-21"></a>Neuerungen bei TSPI Version 2,1

Beginnend mit TAPI 2,1 können die Benutzeroberflächen-DLLs des Telefoniedienstanbieters zum Verwalten und Anzeigen von Dialogfeldern verwendet werden. TAPI lädt die dll in den Prozess einer Anwendung, die eine beliebige Dienstanbieter Funktion aufruft, die ein Dialogfeld anzeigen kann.

Ab TAPI 2,1 können Proxy Anforderungs Handler implementiert werden. Ein Handler ist eine vollständige Telefonieanwendung, die normalerweise auf einem Telefonieserver ausgeführt wird und Dienste bereitstellt, die in einer Anwendung besser implementiert sind als ein Treiber.

Funktionen und Nachrichten, die für TSPI Version 2,1 neu oder geändert wurden, lauten wie folgt:

-   [**TSPI_lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   **TSPI_lineDropNoOwner**–**veraltet**
-   **TSPI_lineDropOnClose**–**veraltet**
-   [**TSPI_lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI_lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI_lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI_lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [**TSPI_lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI_phoneGetID**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [**TSPI_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [**TSPI_providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   [**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))
-   [**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))
-   [**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))
-   [**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))
-   [**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))
-   [**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))
-   [**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))

Die Benutzeroberflächen-DLL des Telefoniedienstanbieters bietet eine Möglichkeit, Benutzerinteraktionen im Kontext der Anwendung anstelle des Dienstanbieters selbst zuzulassen. TSPI Version 2,1 hat die folgenden neuen Funktionen, Meldungen und Strukturen für die Implementierung bereitgestellt:

-   [**TSPI_providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [**TSPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [**TSPI_providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [**TUISPI_lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [**TUISPI_lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [**TUISPI_phoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [**TUISPI_providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [**TUISPI_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [**TUISPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [**TUISPI_providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [**TUISPI_providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [**"Tuispikreatedialoginstanceparameginstancepara"**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [**Tuispidllcallback**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [**LINE_CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
-   [**LINE_SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md)

 

 
