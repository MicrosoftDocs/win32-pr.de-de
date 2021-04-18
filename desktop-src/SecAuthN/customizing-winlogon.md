---
description: Anpassen des Winlogon-Verhaltens durch Implementieren eines Anmelde Informationsanbieters.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Anpassen von Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357393"
---
# <a name="customizing-winlogon"></a>Anpassen von Winlogon

Anpassen des [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Verhaltens durch Implementieren eines Anmelde Informationsanbieters. Weitere Informationen zu Anmelde Informationsanbietern finden Sie unter [**ikredentialprovider-Schnittstelle**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).

**Windows Server 2003 und Windows XP:** Anmelde Informationsanbieter werden nicht unterstützt.

In den folgenden Abschnitten werden Möglichkeiten zum Anpassen von Winlogon in Windows-Versionen vor Windows Vista beschrieben.

> [!Note]  
> Gina-DLLs und Winlogon-Benachrichtigungs Pakete werden in Windows Vista ignoriert.

 

-   [Winlogon-Benachrichtigungs Pakete](#winlogon-notification-packages)
-   [Gina-Stub](#gina-stubs)
-   [Gina-Hooks](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Winlogon-Benachrichtigungs Pakete

Ein Winlogon-Benachrichtigungs Paket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse verarbeiten. Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon jedes Benachrichtigungs Paket auf, um Informationen zum Ereignis bereitzustellen. Weitere Informationen finden Sie unter [Winlogon-Benachrichtigungs Pakete](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>Gina-Stub

Ein [*Gina*](/windows/desktop/SecGloss/g-gly) Stub ist eine benutzerdefinierte GINA-DLL, die die Export Funktions Implementierungen einer zuvor installierten Gina-DLL verwendet (in der Regel MsGina.dll). Ein Gina-Stub ruft Zeiger auf jede Funktion ab, die von der zuvor installierten Gina-DLL exportiert wurde. Jede Gina Stub-Funktion verwendet dann den passenden Funktionszeiger, um die entsprechende Funktion in der zuvor installierten Gina-DLL aufzurufen.

> [!IMPORTANT]
> Jede Gina Stub-Funktion muss die entsprechende Funktion in der zuvor installierten Gina aufruft.

 

Eine Gina Stub-Funktion kann zusätzliche Funktionen in einer oder mehreren ihrer Exportfunktionen implementieren. Beispielsweise kann die [**wlxloggedoutsas**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) -Funktion eines Gina Stub die aktuelle Zeit überprüfen, bevor die **wlxloggedoutsas** -Funktion des MsGina.dll aufgerufen wird. Wenn sich die aktuelle Zeit in einem bestimmten Bereich befunden hat, könnte die stubfunktion eine Meldung anzeigen, die angibt, dass die Anmeldung während dieses Zeitraums nicht zulässig ist, und die **wlx- \_ SAS- \_ Aktion " \_ None** " an "Winlogon" zurückgeben Die **wlxloggedoutsas** -Funktion des MsGina.dll würde dann nur während des zulässigen Zeitraums aufgerufen werden.

Die Gina Stub-Anwendung ruft über den *pwinlogonfunctions* -Parameter der [**wlxinitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) -Funktion eine dispatchtabelle an die Winlogon-Unterstützungsfunktionen ab. Die Gina Stub-Anwendung kann diese Dispatch-Tabelle verwenden, um Winlogon-Unterstützungsfunktionen aufzurufen. Eine Gina Stub-Anwendung kann z. b. die [**wlxsasnotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) -Funktion aufgerufen werden, um ein Sicherheits Ereignis ( [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) , SAS) auszulösen, wenn eine [*Smartcard*](/windows/desktop/SecGloss/s-gly) in einen [*Reader*](/windows/desktop/SecGloss/r-gly)eingefügt wird.

Weitere Informationen zum Erstellen eines Gina Stub finden Sie im Beispiel "Gina Stubs" im \\ Verzeichnis "Beispiele \\ Security \\ Gina \\ Ginastub" einer Platform Software Development Kit (SDK)-Installation.

> [!Note]  
> Alle Aufrufe zwischen einer Gina und Winlogon müssen sich innerhalb eines einzelnen Threads befinden.

 

## <a name="gina-hooks"></a>Gina-Hooks

Ein Gina-Hook ist ein Gina-Stub, der in der Implementierung der [**wlxinitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) -Funktion den Zeiger auf die [**wlxdialogboxparam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) -Unterstützungsfunktion in der dispatchtabelle durch einen Zeiger auf seine eigene Implementierung der **wlxdialogboxparam** -Funktion ersetzt. Daher wird jedes Mal, wenn die zuvor installierte Gina (in der Regel MsGina.dll) die **wlxdialogboxparam** -Funktion aufruft, die durch den Gina-Hook implementierte Funktion aufgerufen.

Die vom Gina-Hook implementierte [**wlxdialogboxparam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) -Funktion kann die [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) -Rückruf Prozedur ersetzen, die auf ein bestimmtes Dialogfeld Ereignis antwortet.

Dadurch erhält der Gina-Hook vollständige Kontrolle über die Darstellung und das Verhalten aller Dialogfelder, die von MsGina.dll erstellt werden.

Weitere Informationen zum Erstellen eines Gina-Hooks finden Sie im Beispiel "Gina Hooks" \\ im \\ Verzeichnis "Beispiele Security \\ Gina \\ ginahook" einer Platform SDK-Installation.

> [!Note]  
> Alle Aufrufe zwischen einer Gina und Winlogon müssen sich innerhalb eines einzelnen Threads befinden.

 

 

 
