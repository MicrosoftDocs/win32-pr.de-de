---
description: Anwendungen, die CAPICOM-Objekte verwenden, müssen mit CAPICOM.dll erstellt werden. CAPICOM.dll müssen auch zur Laufzeit vorhanden und registriert sein, um CAPICOM-Objekte zu verwenden.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Vorbereiten der Verwendung von CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366089"
---
# <a name="getting-ready-to-use-capicom"></a>Vorbereiten der Verwendung von CAPICOM

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Anwendungen, die CAPICOM-Objekte verwenden, müssen mit CAPICOM.dll erstellt werden. CAPICOM.dll müssen auch zur Laufzeit vorhanden und registriert sein, um CAPICOM-Objekte zu verwenden. CAPICOM.dll sollten Visual Basic Projekt verweisen hinzugefügt werden, um CAPICOM-Objekte zu verwenden.

CAPICOM ist als verteilbare Datei verfügbar, die von [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281)heruntergeladen werden kann. Informationen zu CAPICOM-Versionen finden Sie unter [CAPICOM-Versionen](capicom-versions.md).

**So registrieren Sie CAPICOM.dll**

-   Wechseln Sie an einer Eingabeaufforderung in das Verzeichnis, in dem CAPICOM.dll gespeichert ist, und geben Sie dann den folgenden Befehl ein:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Einschränkungen für Code Beispiele

Um präziseren, besser lesbaren Code bereitzustellen, werden die Prinzipien der bewährten Programmierpraxis nicht immer in diesen Beispielen befolgt. Insbesondere werden nur eingeschränkte Fehler Antworten angezeigt. Funktionierende Anwendungen sollten die zurückgegebenen Fehlercodes immer überprüfen und geeignete Aktionen ausführen, wenn ein Fehler auftritt.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Erforderliche Schlüssel Container, Schlüssel und Zertifikate in CAPICOM

Einige Vorgänge mit CAPICOM-Objekten können von jedem beliebigen Benutzer auf jedem Computer durchgeführt werden. das Erstellen [*digitaler Signaturen*](../secgloss/d-gly.md) und das Abrufen des Klartext-Inhalts einer eingeschlossenen Nachricht mithilfe von CAPICOM-Objekten sind Zertifikat basierte Vorgänge. Der Benutzer, der eine digitale Signatur erstellt, und der Benutzer, der den verschlüsselten Inhalt einer eingeschlossenen Nachricht abruft, müssen über ein digitales Zertifikat mit einem verfügbaren zugeordneten privaten Schlüssel verfügen. Wenn kein Zertifikat mit einem zugeordneten privaten Schlüssel vorhanden ist, kann der Kryptografievorgang nicht ausgeführt werden. Benutzer von CAPICOM-Anwendungen müssen sicherstellen, dass Sie über das geeignete Zertifikat und den verfügbaren privaten Schlüssel verfügen, wenn die Anwendungen ausgeführt werden.

Einige Beispiele in den folgenden Abschnitten führen Vorgänge aus, die ein verfügbares [*öffentliches/privates Schlüsselpaar*](../secgloss/p-gly.md) zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen erfordern. Viele dieser Programme werden kompiliert und ausgeführt, schlagen aber zur Laufzeit fehl, ohne dass in diesen speichern ordnungsgemäße [*Schlüssel Container*](../secgloss/k-gly.md), Schlüssel, Zertifikat Speicher und [*Zertifikate*](../secgloss/c-gly.md) vorhanden sind.

**So erstellen Sie ein selbstsigniertes Zertifikat**

1.  Installieren Sie die Signierungs Tools. Diese werden als Teil des Microsoft Windows Software Development Kit (SDK), des Platform Software Development Kit (SDK) oder des .NET Framework SDK installiert.
2.  Nachdem Makecert.exe heruntergeladen wurde, führen Sie den folgenden Befehl an einer Eingabeaufforderung aus, indem Sie einen Benutzernamen für *username*, einen Organisationsnamen für *OrganizationName* und einen Firmennamen für *CompanyName* ersetzen:

    **Makecert-r-n "CN =**_username_*_, ou =_*_OrganizationName_*_, o =_*_CompanyName_*_"-SS My_*

3.  Das Zertifikat kann im My-Speicher des aktuellen Benutzers abgelegt werden. Importieren Sie das erstellte Zertifikat in den Stamm Speicher, damit es als vertrauenswürdig eingestuft wird.

 

 
