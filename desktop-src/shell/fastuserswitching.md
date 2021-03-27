---
description: Windows XP-Benutzerkonten ermöglichen es, dass mehrere Benutzer gleichzeitig angemeldet sind, jeweils mit ihren eigenen Einstellungen und jeweils mit ihren eigenen Anwendungen.
ms.assetid: bc404afc-f73e-404d-854d-faab5cf205a5
title: Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc26471bcf56efce79fb5ccc91a78c24e43ae312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994767"
---
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a>Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop

Windows XP-Benutzerkonten ermöglichen es, dass mehrere Benutzer gleichzeitig angemeldet sind, jeweils mit ihren eigenen Einstellungen und jeweils mit ihren eigenen Anwendungen. Da sich ein Benutzer nicht anmelden muss, um den Zugriff auf einen anderen Benutzer zuzulassen, kann auf den Desktop eines Benutzers problemlos mithilfe der Funktion für schnelles Benutzer wechseln zugegriffen werden. Benutzerkonten enthalten auch die persönliche Terminal Server Funktion oder Remotedesktop, mit der Benutzer über Remote Systeme auf Ihr Desktop Konto zugreifen können.

Die folgenden Themen werden erörtert.

-   [Anforderungen an die Infrastruktur Verwendung](#infrastructure-usage-requirements)
-   [Kompatibilität mit vorhandenen Anwendungen](#compatibility-with-existing-applications)
-   [Registrieren für Sitzungs Wechsel Benachrichtigung](#registering-for-session-switching-notification)
-   [Es wird sichergestellt, dass nur eine Instanz der Anwendung ausgeführt wird.](#ensuring-only-one-instance-of-your-application-is-running)
-   [Herunterfahren der Anwendung über alle Sitzungen hinweg](#shutting-down-your-application-across-all-sessions)
-   [Interaktion mit System Diensten](#interaction-with-system-services)
-   [Remotedesktop und Bandbreite](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a>Anforderungen an die Infrastruktur Verwendung

Die zugrunde liegende Infrastruktur, die von Windows 2000 geerbt wird, unterstützt die Zustands Trennung von Benutzerdaten, Benutzereinstellungen und Computereinstellungen. Wenn Sie diese Infrastruktur nutzen, sind die folgenden Schritte erforderlich, um Ihre Anwendung unter Windows XP erfolgreich auszuführen.

-   Standardmäßig den Ordner " **eigene** Dateien" für die Speicherung von Benutzer erstellten Daten.
-   Klassifizieren und Speichern von Anwendungsdaten ordnungsgemäß.
-   "Zugriff verweigert"-Meldungen ordnungsgemäß herabstufen.

Temporäre Dateien, im Speicher abgebildete Dateien und Dokumente sollten im entsprechenden Unterverzeichnis des Benutzerprofil Verzeichnisses gespeichert werden. Verwenden Sie " [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) " oder " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ", um den entsprechenden Speicherort für diese Dateien zu ermitteln. Wenn Sie das [**CSIDL \_ AppData**](csidl.md) -Flag an diese Funktionen übergeben, wird der Pfad eines Dateisystem Verzeichnisses zurückgegeben, das als gängiges Repository für anwendungsspezifische Daten fungiert. Verwenden Sie das Flag [**CSIDL \_ local \_ AppData**](csidl.md) anstelle von **CSIDL \_ AppData** für Daten, die sich ändern sollen, wenn sich der Benutzer ändert, z. b. temporäre Dateien.

Bei den oben aufgeführten Anforderungen handelt es sich um eine Teilmenge der im Microsoft-Zertifizierungsprogramm aufgeführten Anforderungen. Weitere Informationen finden Sie auf der Seite " **Certified for Windows Program** " unter https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx .

## <a name="compatibility-with-existing-applications"></a>Kompatibilität mit vorhandenen Anwendungen

Sowohl der schnelle Benutzerwechsel als auch der persönliche Terminal Server verwenden die Terminaldienstetechnologie und sind daher mit den meisten früheren Microsoft Win32-Anwendungen kompatibel. Wenn eine Anwendung mit Windows 2000-Logo kompatibel ist und die grundlegenden profile Trennung und Energie Verwaltungsfunktionen implementiert, sollte diese Anwendung ordnungsgemäß unter den einzelnen Windows XP-Benutzerkonten ausgeführt werden.

## <a name="registering-for-session-switching-notification"></a>Registrieren für Sitzungs Wechsel Benachrichtigung

In der Regel muss eine Anwendung nicht benachrichtigt werden, wenn ein Desktop Switch auftritt. Anwendungen, die benachrichtigt werden müssen, wenn das Konto, unter dem Sie ausgeführt werden, der aktuelle Desktop ist, z. b. Anwendungen, die auf den seriellen Anschluss oder andere freigegebene Ressourcen zugreifen, können sich für die Benachrichtigung über den Desktop Switch registrieren. Um sich für eine Benachrichtigung zu registrieren, verwenden Sie die [**Wout registersessionnotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) -Funktion.

Nachdem diese Funktion aufgerufen wurde, wird das Fenster mit dem *HWND* -handle registriert, um eine [**WM- \_ wtssession- \_ Änderungs**](../termserv/wm-wtssession-change.md) Nachricht über seine **WndProc** -Funktion zu empfangen. Die Sitzungs-ID wird im **LPARAM** -Parameter gesendet, und ein Code, der das Ereignis angibt, das die Nachricht generiert hat, wird in **wParam** als eines der folgenden Flags gesendet.

-   WTS \_ Console \_ Connect
-   Trennen der WTS- \_ Konsole \_
-   WTS \_ Remote \_ Connect
-   WTS \_ Remote \_ Disconnect
-   Logo der WTS- \_ Sitzung \_
-   Anmelde der WTS- \_ Sitzung \_

Anwendungen können diese Nachricht verwenden, um Ihren Status zu überprüfen und um Konsolen spezifische Ressourcen freizugeben und zu erhalten. Benutzer Desktops können zwischen Remote-und Konsolen Steuerung dynamisch gewechselt werden. Anwendungen sollten die [**WM- \_ wtssession- \_ Änderungs**](../termserv/wm-wtssession-change.md) Meldung verwenden, um eine Synchronisierung mit dem Remote-oder lokalen Verbindungsstatus auszuführen.

Wenn Ihr Prozess diese Benachrichtigungen nicht mehr benötigt oder beendet wird, sollte [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) aufgerufen werden, um die Registrierung der Benachrichtigung aufzuheben.

> [!IMPORTANT]
> Die an [**wzregistersessionnotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) weiter gegebenen **HWND** -Werte sind Verweis gezählt. Daher müssen Sie die gleiche Anzahl von Aufrufen an [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) vornehmen, um die Freigabe aller zugeordneten Ressourcen sicherzustellen.

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a>Es wird sichergestellt, dass nur eine Instanz der Anwendung ausgeführt wird.

Viele Anwendungen müssen sicherstellen, dass nur eine Instanz ausgeführt wird. Es gibt mehrere Möglichkeiten, dies in Windows XP zu tun. Dazu zählen die folgenden:

-   Verwenden Sie [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) oder [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) , um nach einem bekannten Fenster zu suchen, das von der Anwendung geöffnet wird. Wenn dieses Fenster bereits geöffnet ist, können Sie es als Hinweis darauf verwenden, dass die Anwendung bereits ausgeführt wird.
-   Erstellen Sie ein Mutex-oder Semaphor-Objekt, wenn die Anwendung geöffnet ist, und schließen Sie dieses Objekt, wenn die Anwendung beendet wird. Der globale Objekt Namespace ist für jeden Desktop getrennt und ermöglicht eine eindeutige Liste von Mutex-und Semaphor-Objekten.

## <a name="shutting-down-your-application-across-all-sessions"></a>Herunterfahren der Anwendung über alle Sitzungen hinweg

Eine Anwendung muss möglicherweise über alle Sitzungen hinweg heruntergefahren werden. Beispielsweise kann eine Anwendung, die in zwei oder mehr Sitzungen gleichzeitig ausgeführt wird, eine neue Datei aus dem Web herunterladen. Anschließend muss er sich selbst schließen und mit den aktualisierten Bits neu starten. Dies müsste natürlich in allen laufenden Sitzungen erfolgen. Die Anwendung muss so geschrieben werden, dass Sie ordnungsgemäß beendet wird, wenn eine Benachrichtigung empfangen wird.

## <a name="interaction-with-system-services"></a>Interaktion mit System Diensten

Aus programmatischen Sicht müssen die folgenden Fälle behandelt werden.

-   Der Server Prozess empfängt eine direkte Anforderung von einem Client Prozess.

    In diesem Fall wird die Nachricht wahrscheinlich mithilfe eines lokalen Prozedur Aufrufs (Local Procedure Call, LPC) oder eines Remote Prozedur Aufrufs (RPC) übertragen. Es gibt APIs für den LPC oder RPC, die das Abrufen des Client Tokens ermöglichen. Sobald das Client Token abgerufen wurde, kann der Server es in einem aufzurufenden aufrufungsserver [**verwenden.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Dadurch wird der Prozess auf der richtigen Fenster Station angezeigt, vorausgesetzt, dass das Client Benutzer Token über ein Sitzungstag verfügt.

    > [!Note]  
    > " [**Comateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " unterstützt zu diesem Zeitpunkt keine Sitzungs übergreifende Vererbung.

     

-   Der Server Prozess erhält eine Benachrichtigung und muss die Benutzeroberfläche anzeigen, die Anzeige muss sich jedoch nicht im Kontext des aktuellen Benutzers befinden.

    In diesem Fall kann der Server Prozess sein primäres Prozess Token duplizieren und den fraglichen Sitzungs Bezeichner so ändern, dass er mit dem aktuellen Sitzungs Bezeichner identisch ist. Der aktuelle Sitzungs Bezeichner kann mithilfe der [**wzgetactiveconsolesessionid**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) -Funktion abgerufen werden.

    > [!Note]  
    > Um die tokensitzungs-ID festzulegen, benötigen Sie die **SE \_ TCB- \_ Berechtigung**. Dies erfolgt nur als Dienst, der im NT Authority System ausgeführt wird \\ .

     

## <a name="remote-desktop-and-bandwidth"></a>Remotedesktop und Bandbreite

Durch das Hinzufügen des Remotedesktop Features zu Windows XP sollten Anwendungen nicht mehr Bandbreite als nötig verwenden, sodass Sie umfassende Bildschirm Zeichnungen und Animationseffekte vermeiden, wenn der Desktop Remote verbunden ist. Um zu ermitteln, ob die aktuelle Sitzung Remote ist, können Sie [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit **SM \_ remotesession** aufrufen. Beachten Sie jedoch, dass dieser-Befehl nicht zwischen Remote und getrennt unterscheidet.

 

 
