---
description: Verwenden Sie kryptografische Technologien für die Verschlüsselung mit öffentlichem Schlüssel, Verschlüsselungsalgorithmen, RSA-Verschlüsselung und digitale Zertifikate.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Kryptografie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050f84d118cb5ad9e1da49ddabd73489745339bb0b1357e229b0f1609a1c997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876110"
---
# <a name="cryptography"></a>Kryptografie

## <a name="purpose"></a>Zweck

Kryptografie ist die Verwendung von Codes zum Konvertieren von Daten, sodass nur ein bestimmter Empfänger sie mithilfe eines Schlüssels lesen kann.

Zu den Kryptotechnologien von Microsoft gehören CryptoAPI, Kryptografiedienstanbieter (Cryptographic Service Providers, CSP), CryptoAPI-Tools, CAPICOM, WinTrust, das Ausstellen und Verwalten von Zertifikaten und die Entwicklung anpassbarer Public Key-Infrastrukturen. Die Registrierung von Zertifikaten und Smartcards, die Zertifikatverwaltung und die Entwicklung benutzerdefinierter Module werden ebenfalls beschrieben.

## <a name="developer-audience"></a>Entwicklergruppe

CryptoAPI ist für die Verwendung durch Entwickler von Windows-basierten Anwendungen vorgesehen, mit denen Benutzer Dokumente und andere Daten in einer sicheren Umgebung erstellen und austauschen können, insbesondere über unsichere Medien wie das Internet. Entwickler sollten mit den Programmiersprachen C und C++ und der Windows Programmierumgebung vertraut sein. Obwohl dies nicht erforderlich ist, wird empfohlen, kryptografie- oder sicherheitsbezogene Themen zu verstehen.

CAPICOM ist eine nur 32-Bit-Komponente, die für Entwickler vorgesehen ist, die Anwendungen mithilfe Visual Basic VbScript-Programmiersprache (Scripting Edition) oder C++-Programmiersprache erstellen. CAPICOM ist für die Verwendung in den Betriebssystemen verfügbar, die in Run-Time Requirements angegeben sind. Für die zukünftige Entwicklung empfiehlt es sich, die .NET Framework zu verwenden, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.

CAPICOM 2.1.0.2 wird unter den folgenden Betriebssystemen und Versionen unterstützt:

-   Windows Server 2003
-   Windows XP

CAPICOM ist als verteilbare Datei verfügbar, die von Platform SDK Redistributable heruntergeladen werden [kann: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).

Für Zertifikatdienste sind die folgenden Versionen dieser Betriebssysteme erforderlich:

-   Windows Server 2008 R2
-   WindowsServer 2008
-   Windows Server 2003

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                           | BESCHREIBUNG                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zur Kryptografie](about-cryptography.md)<br/>         | Wichtige Kryptografiekonzepte und eine grundlegende Ansicht der Microsoft-Kryptografietechnologien.<br/>                                                                                                                           |
| [Verwenden der Kryptografie](using-cryptography.md)<br/>         | Kryptografieprozesse, Prozeduren und erweiterte Beispiele von C- und Visual Basic Programmen, die CryptoAPI-Funktionen und CAPICOM-Objekte verwenden.<br/>                                                                            |
| [Kryptografiereferenz](cryptography-reference.md)<br/> | Ausführliche Beschreibungen der Kryptografiefunktionen, Schnittstellen, Objekte, Strukturen und anderen Programmierelemente von Microsoft. Enthält Referenzbeschreibungen der API für die Arbeit mit digitalen Zertifikaten.<br/> |



 

 

 




