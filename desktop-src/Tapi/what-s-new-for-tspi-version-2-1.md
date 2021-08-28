---
description: Ab TAPI 2.1 können die Benutzeroberflächen-DLLs des Telefoniedienstanbieters zum Verwalten und Anzeigen von Dialogfeldern verwendet werden. TAPI lädt die DLL in den Prozess einer Anwendung, die eine der Dienstanbieterfunktionen aufruft, die ein Dialogfeld anzeigen können.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Neues bei TSPI Version 2.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260978ad99bf49ed0beae0e71b2a02a794eef1a7af0c25074c20a08c1da054c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659820"
---
# <a name="whats-new-for-tspi-version-21"></a>Neues bei TSPI Version 2.1

Ab TAPI 2.1 können die Benutzeroberflächen-DLLs des Telefoniedienstanbieters zum Verwalten und Anzeigen von Dialogfeldern verwendet werden. TAPI lädt die DLL in den Prozess einer Anwendung, die eine der Dienstanbieterfunktionen aufruft, die ein Dialogfeld anzeigen können.

Ab TAPI 2.1 können Proxyanforderungshandler implementiert werden. Ein Handler ist eine vollständige Telefonieanwendung, die normalerweise auf einem Telefonieserver ausgeführt wird und Dienste bietet, die in einer Anwendung besser implementiert sind als ein Treiber.

Funktionen und Meldungen, die für TSPI Version 2.1 neu oder geändert wurden, lauten wie folgt:

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

Die Benutzeroberflächen-DLL des Telefoniedienstanbieters bietet eine Möglichkeit, die Benutzerinteraktion im Kontext der Anwendung statt des Dienstanbieters selbst zu ermöglichen. TSPI Version 2.1 lieferte die folgenden neuen Funktionen, Meldungen und Strukturen für die Implementierung:

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
-   [**STENSPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [**RATESSPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [**LINE_CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
-   [**LINE_SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md)

 

 
