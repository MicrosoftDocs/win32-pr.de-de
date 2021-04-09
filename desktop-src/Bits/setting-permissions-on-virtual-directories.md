---
title: Festlegen von Berechtigungen für virtuelle Verzeichnisse
description: Aus Sicherheitsgründen werden von Background Intelligent Transfer Service (Bits) keine Dateien in ein virtuelles Verzeichnis hochgeladen, für das Skript-und Ausführungs Berechtigungen aktiviert sind.
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039208"
---
# <a name="setting-permissions-on-virtual-directories"></a>Festlegen von Berechtigungen für virtuelle Verzeichnisse

Aus Sicherheitsgründen werden von Background Intelligent Transfer Service (Bits) keine Dateien in ein virtuelles Verzeichnis hochgeladen, für das Skript-und Ausführungs Berechtigungen aktiviert sind. Wenn Sie eine Datei in ein virtuelles Verzeichnis hochladen, für das diese Berechtigungen aktiviert sind, schlägt der Auftrag mit dem Fehlercode "BG \_ E \_ Server EXECUTE" ( \_ Ausführung aktiviert) fehl \_ .

Bits erfordert nicht, dass das virtuelle Verzeichnis Schreib fähig ist. Daher empfiehlt es sich, den Schreibzugriff auf das virtuelle Verzeichnis zu deaktivieren.

Der authentifizierte Benutzer (oder der anonyme Benutzer von IIS für die anonyme Authentifizierung) muss über die Berechtigung "ändern" für das physische Verzeichnis verfügen, dem das virtuelle Verzeichnis zugeordnet ist. das Erteilen von Schreibberechtigungen ist nicht ausreichend.

## <a name="specifying-permissions-for-notifications"></a>Angeben von Berechtigungen für Benachrichtigungen

Das Authentifizierungsschema, das Sie für das virtuelle Verzeichnis und die Benachrichtigungs-URL angeben (siehe [bitsservernotificationurl](bits-iis-extension-properties.md) -Eigenschaft), muss kompatibel sein. Bits verwendet das für das virtuelle Verzeichnis angegebene Authentifizierungsschema für den Zugriff auf die Benachrichtigungs-URL. Der Uploadauftrag schlägt fehl, wenn Bits aufgrund eines Authentifizierungsfehlers nicht auf die Benachrichtigungs-URL zugreifen kann.

Wenn der Benachrichtigungstyp (siehe die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) ) als [Verweis](using-bits-notification-request-response-headers.md)bezeichnet wird, muss die Anwendung sicherstellen, dass der Benutzer Zugriff auf die Datei hat, auf die verwiesen wird (siehe den Header [Bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) ). Bits legt die ACLs in der referenzierten Datei auf diejenigen des physischen Verzeichnisses fest, dem das virtuelle Verzeichnis zugeordnet ist.

> [!Note]  
> Die Benachrichtigungs Anwendung muss in der Lage sein, die Remote Datei zuzuordnen und auf diese zuzugreifen, auch wenn die Benachrichtigungs-URL von einem Webserver bedient wird, der sich auf einem anderen Computer als das physische Uploadverzeichnis befindet. Der Header [Bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) enthält immer eine Pfadspezifikation, die relativ zu dem Computer ist, der die Komponente Bits-Erweiterungen gehostet. Eine Anwendung, die auf einem anderen Computer ausgeführt wird, muss möglicherweise den Pfad vor dem Zugriff in einen UNC-Pfad konvertieren.

 

Bits unterstützt viele Kombinationen von Authentifizierungs Schemas. Sie sollten jedoch das folgende Authentifizierungsschema für das virtuelle Verzeichnis und die übereinstimmende Benachrichtigungs-URL verwenden.

-   Um durch Verweis Benachrichtigungen zu unterstützen, sollte das virtuelle Verzeichnis für die Verwendung der NTLM-Authentifizierung (Aushandlung) konfiguriert werden, wenn das Verzeichnis für physische Uploads (das Verzeichnis, in dem die virtuellen Verzeichnis Punkte angezeigt werden) ein anderes Authentifizierungsschema als anonym verwendet. Wenn das Verzeichnis für physische Uploads anonyme Anforderungen zulässt (keine Authentifizierung), sollte das virtuelle Verzeichnis Anonym (keine Authentifizierung) aktivieren.

    Die ACLs im Verzeichnis für physische Uploads müssen so festgelegt werden, dass der authentifizierte Benutzer Dateien in dem Verzeichnis lesen kann, auf das die Benachrichtigungs-URL verweist. Bits verwendet die ACLs des physischen Uploads-Verzeichnisses, um die ACLs der temporären Uploaddatei festzulegen (der Header " [Bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) " enthält den Pfad zur temporären Datei).

-   Da Benachrichtigungen [nach Wert](using-bits-notification-request-response-headers.md) nicht erfordern, dass die Benachrichtigungs Anwendung auf eine temporäre Datei, die den uploadinhalt enthält, zugreifen kann, kann das Authentifizierungsschema entweder anonym oder Aushandlungs (NTLM) sein. Die einzige Voraussetzung ist, dass der authentifizierte Benutzer für das virtuelle Verzeichnis ebenfalls autorisiert werden muss, um auf die Benachrichtigungs-URL zuzugreifen.

## <a name="specifying-permissions-for-remote-shares"></a>Angeben von Berechtigungen für Remote Freigaben

Ein virtuelles Verzeichnis kann auf ein zugeordnetes Laufwerk auf einem anderen Computer oder einer Netzwerkfreigabe verweisen. Wenn Sie auf ein zugeordnetes Netzwerklaufwerk zeigt, sollten die Anmelde Informationen für die Zuordnung des Laufwerks über Vollzugriff auf die Remote Freigabe verfügen.

Wenn das virtuelle Verzeichnis auf eine Netzwerkfreigabe verweist, verwendet Bits die Verbindung des virtuellen Verzeichnisses **als** Benutzer Anmelde Informationen für den Zugriff auf die Remote Freigabe. Für den Zugriff auf eine Remote Freigabe benötigt das **Connect as** -Konto Berechtigungen, wie in der Dokumentation für die [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) -Funktion beschrieben. Bits meldet sich mithilfe der \_ \_ \_ interaktiven Anmelde Typen LOGON32 Logon Batch oder LOGON32 LOGON an \_ . Das **Connect as** -Benutzerkonto benötigt Full-Access Berechtigungen für die Remote Freigabe. das Erteilen von Schreibberechtigungen ist nicht ausreichend.

Wenn das physische Uploadverzeichnis einer Netzwerkfreigabe zugeordnet ist, ist die Identität des Aufrufers, der die Benachrichtigungs-URL anfordert, entweder der **Connect as** -Benutzer oder der authentifizierte Benutzer des physischen Uploadverzeichnisses (nur verfügbar in IIS 6,0 und höher), wenn im Dialogfeld " **Verbinden als** " immer die Anmelde Informationen des **authentifizierten Benutzers verwendet** werden.

 

 