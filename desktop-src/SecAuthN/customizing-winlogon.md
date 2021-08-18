---
description: Passen Sie das Winlogon-Verhalten an, indem Sie eine Anmeldeinformationsanbieter.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Anpassen der Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10b2ae1e029bb741a2402a25d8e51f331fdd1cac1e9918dfef3b35b36c8e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008658"
---
# <a name="customizing-winlogon"></a>Anpassen der Winlogon

Anpassen [*des Winlogon-Verhaltens*](/windows/desktop/SecGloss/w-gly) durch Implementieren eines Anmeldeinformationsanbieter. Informationen zu Anmeldeinformationsanbietern finden Sie unter [**ICredentialProvider-Schnittstelle**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).

**Windows Server 2003 und Windows XP:** Anmeldeinformationsanbieter werden nicht unterstützt.

In den folgenden Abschnitten werden Möglichkeiten zum Anpassen der Winlogon in Windows Versionen vor Windows Vista beschrieben.

> [!Note]  
> GINA-DLLs und Winlogon-Benachrichtigungspakete werden in Windows Vista ignoriert.

 

-   [Winlogon-Benachrichtigungspakete](#winlogon-notification-packages)
-   [GINA-Stubs](#gina-stubs)
-   [GINA-Hooks](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Winlogon-Benachrichtigungspakete

Ein Winlogon-Benachrichtigungspaket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse behandeln. Wenn sich beispielsweise ein Benutzer beim System anmeldet, ruft Winlogon jedes Benachrichtigungspaket auf, um Informationen zum Ereignis zu liefern. Weitere Informationen finden Sie unter [Winlogon Notification Packages](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>GINA-Stubs

Ein [*GINA-Stub*](/windows/desktop/SecGloss/g-gly) ist eine benutzerdefinierte GINA-DLL, die die Implementierungen der Exportfunktion einer zuvor installierten GINA-DLL verwendet (in der Regel MsGina.dll). Ein GINA-Stub ruft Zeiger auf jede Funktion ab, die von der zuvor installierten GINA-DLL exportiert wird. Jede GINA-Stubfunktion verwendet dann den entsprechenden Funktionszeiger zum Aufrufen der entsprechenden Funktion in der zuvor installierten GINA-DLL.

> [!IMPORTANT]
> Jede GINA-Stubfunktion muss die entsprechende Funktion in der zuvor installierten GINA aufrufen.

 

Eine GINA-Stubfunktion kann zusätzliche Funktionen in eine oder mehrere ihrer Exportfunktionen implementieren. Beispielsweise kann die [**WlxLoggedOutSAS-Funktion**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) eines GINA-Stubs die aktuelle Zeit überprüfen, bevor die **WlxLoggedOutSAS-Funktion** des -MsGina.dll. Wenn die aktuelle Zeit innerhalb eines bestimmten Bereichs liegt, könnte die Stubfunktion eine Meldung anzeigen, die angibt, dass die Anmeldung während dieses Zeitraums nicht mehr unterstützt wird, und **WLX \_ SAS \_ ACTION \_ NONE** an Winlogon zurückgeben. Die **WlxLoggedOutSAS-Funktion** des MsGina.dll dann nur während des zulässigen Zeitraums aufgerufen.

Die GINA-Stubanwendung ruft über den *pWinlogonFunctions-Parameter* der [**WlxInitialize-Funktion**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) eine Dispatchtabelle für Winlogon-Unterstützungsfunktionen ab. Die GINA-Stubanwendung kann diese Dispatchtabelle zum Aufrufen von Winlogon-Unterstützungsfunktionen verwenden. Beispielsweise kann eine GINA-Stubanwendung die [**WlxSasNotify-Funktion**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) aufrufen, um ein [](/windows/desktop/SecGloss/s-gly) SAS-Ereignis [*(Secure Attention Sequence)*](/windows/desktop/SecGloss/s-gly) zu verursachen, wenn eine Smartcard in einen Reader [*eingefügt wird.*](/windows/desktop/SecGloss/r-gly)

Weitere Informationen zum Erstellen eines GINA-Stubs finden Sie im Gina Stubs-Beispiel im Verzeichnis \\ Samples \\ Security \\ \\ GinaStub einer Platform Software Development Kit -Installation (SDK).

> [!Note]  
> Alle Aufrufe zwischen GINA und Winlogon müssen innerhalb eines einzelnen Threads liegen.

 

## <a name="gina-hooks"></a>GINA-Hooks

Ein GINA-Hook ist ein GINA-Stub, der in seiner Implementierung der [**WlxInitialize-Funktion**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) den Zeiger auf die [**WlxDialogBoxParam-Unterstützungsfunktion**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) in der Dispatchtabelle durch einen Zeiger auf seine eigene Implementierung der **WlxDialogBoxParam-Funktion** ersetzt. Daher wird jedes Mal, wenn die zuvor installierte GINA (in der Regel MsGina.dll) die **WlxDialogBoxParam-Funktion** aufruft, die durch den GINA-Hook implementierte Funktion aufgerufen.

Die vom GINA-Hook implementierte [**WlxDialogBoxParam-Funktion**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) kann die [**DialogProc-Rückrufprozedur**](/windows/win32/api/winuser/nc-winuser-dlgproc) ersetzen, die auf ein bestimmtes Dialogfeldereignis reagiert.

Dadurch erhält der GINA-Hook die vollständige Kontrolle über die Darstellung und das Verhalten aller Dialogfelder, die MsGina.dll werden.

Weitere Informationen zum Erstellen eines GINA-Hooks finden Sie im Gina Hooks-Beispiel im \\ \\ Beispielsicherheitsverzeichnis \\ von Gina \\ GinaHook einer Plattform-SDK-Installation.

> [!Note]  
> Alle Aufrufe zwischen GINA und Winlogon müssen innerhalb eines einzelnen Threads liegen.

 

 

 
