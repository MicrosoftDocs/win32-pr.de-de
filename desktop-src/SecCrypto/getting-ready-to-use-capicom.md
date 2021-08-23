---
description: Anwendungen, die CAPICOM-Objekte verwenden, müssen mithilfe von CAPICOM.dll. CAPICOM.dll müssen auch zur Laufzeit vorhanden und registriert sein, um CAPICOM-Objekte verwenden zu können.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Getting Ready to Use CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a6b76c293395fd0979cf5c304b27bae75622996279bd891b8c0c1301dca82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006629"
---
# <a name="getting-ready-to-use-capicom"></a>Getting Ready to Use CAPICOM

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Anwendungen, die CAPICOM-Objekte verwenden, müssen mithilfe von CAPICOM.dll. CAPICOM.dll müssen auch zur Laufzeit vorhanden und registriert sein, um CAPICOM-Objekte verwenden zu können. CAPICOM.dll sollte den Projektverweisen hinzugefügt Visual Basic, um CAPICOM-Objekte zu verwenden.

CAPICOM ist als verteilbare Datei verfügbar, die unter [Platform SDK Redistributable: CAPICOM heruntergeladen werden kann.](https://www.microsoft.com/download/details.aspx?id=25281) Informationen zu CAPICOM-Versionen finden Sie unter [CAPICOM-Versionen.](capicom-versions.md)

**So registrieren Sie CAPICOM.dll**

-   Ändern Sie an einer Eingabeaufforderung das Verzeichnis in das Verzeichnis, in dem CAPICOM.dll gespeichert ist, und geben Sie dann den folgenden Befehl ein:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Beispielcodeeinschränkungen

Um präziseren, besser lesbaren Code zu bieten, werden die Prinzipien der bewährten Programmiertechnik in diesen Beispielen nicht immer befolgt. Insbesondere werden nur eingeschränkte Fehlerantworten angezeigt. Funktionierende Anwendungen sollten immer zurückgegebene Fehlercodes überprüfen und geeignete Aktionen ausführen, wenn ein Fehler auftritt.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Erforderliche Schlüsselcontainer, Schlüssel und Zertifikate in CAPICOM

Während einige Vorgänge mit CAPICOM-Objekten von jedem [](../secgloss/d-gly.md) Benutzer auf jedem Computer durchgeführt werden können, sind das Erstellen digitaler Signaturen und das Abrufen des Klartextinhalts einer umschlagten Nachricht mithilfe von CAPICOM-Objekten zertifikatbasierte Vorgänge. Der Benutzer, der eine digitale Signatur erstellt, und der Benutzer, der den verschlüsselten Inhalt einer umschlagten Nachricht abruft, müssen über ein digitales Zertifikat mit einem verfügbaren zugeordneten privaten Schlüssel verfügen. Wenn kein Zertifikat mit einem zugeordneten privaten Schlüssel vorhanden ist, kann der kryptografische Vorgang nicht durchgeführt werden. Benutzer von CAPICOM-Anwendungen müssen sicherstellen, dass sie über das entsprechende Zertifikat und den verfügbaren privaten Schlüssel verfügen, wenn die Anwendungen ausgeführt werden.

Einige Beispiele in den folgenden Abschnitten [](../secgloss/p-gly.md) führen Vorgänge aus, die ein verfügbares Paar aus öffentlichem und privatem Schlüssel zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen erfordern. Viele dieser Programme werden kompiliert und ausgeführt, können aber [](../secgloss/k-gly.md)zur Laufzeit nicht ausgeführt werden, ohne dass geeignete Schlüsselcontainer, Schlüssel, [*Zertifikatspeicher*](../secgloss/c-gly.md) und Zertifikate in diesen Speichern vorliegen.

**So erstellen Sie ein selbstsigniertes Zertifikat**

1.  Installieren Sie die Signaturtools. Diese werden als Teil des Microsoft Windows Software Development Kit (SDK), des Platform Software Development Kit (SDK) oder des .NET Framework INSTALLIERT.
2.  Nachdem Makecert.exe heruntergeladen wurde, führen Sie den folgenden Befehl an einer Eingabeaufforderung aus, und geben Sie dabei einen Benutzernamen für *UserName,* einen Organisationsnamen für *OrganizationName* und einen Unternehmensnamen für *CompanyName ein:*

    **makecert -r -n "cn=**_UserName_*_, ou=_*_OrganizationName_*_, o=_*_CompanyName_*_" -ss my_*

3.  Das Zertifikat kann im Speicher Mein des aktuellen Benutzers platziert werden. Importieren Sie das erstellte Zertifikat in den Stammspeicher, damit es vertrauenswürdig ist.

 

 
