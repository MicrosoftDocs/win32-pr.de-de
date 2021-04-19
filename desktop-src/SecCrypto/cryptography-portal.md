---
description: Verwenden Sie Kryptografietechnologien für Verschlüsselung mit öffentlichem Schlüssel, Verschlüsselungsalgorithmen, RSA-Verschlüsselung und digitale Zertifikate.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Kryptografie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350405"
---
# <a name="cryptography"></a>Kryptografie

## <a name="purpose"></a>Zweck

Kryptografie ist die Verwendung von Codes zum Konvertieren von Daten, sodass nur ein bestimmter Empfänger ihn mit einem Schlüssel lesen kann.

Zu den Kryptografietechnologien von Microsoft gehören CryptoAPI, Kryptografiedienstanbieter (CSP), CryptoAPI-Tools, CAPICOM, wintrust, ausstellen und Verwalten von Zertifikaten und entwickeln anpassbarer Public Key-Infrastrukturen. Die Zertifikat-und Smartcard-Registrierung, Zertifikat Verwaltung und die Entwicklung benutzerdefinierter Module werden ebenfalls beschrieben.

## <a name="developer-audience"></a>Entwicklergruppe

CryptoAPI ist für die Verwendung durch Entwickler von Windows-basierten Anwendungen gedacht, die es Benutzern ermöglichen, Dokumente und andere Daten in einer sicheren Umgebung zu erstellen und auszutauschen, insbesondere über nicht sichere Medien wie das Internet. Entwickler sollten mit den Programmiersprachen C und C++ und der Windows-Programmierumgebung vertraut sein. Es ist zwar nicht erforderlich, aber es wird empfohlen, Kryptografie-oder sicherheitsrelevante Themen zu verstehen.

CAPICOM ist eine nur-32-Bit-Komponente, die von Entwicklern verwendet werden kann, die Anwendungen mit Visual Basic Scripting Edition-Programmiersprache (VBScript) oder der Programmiersprache C++ erstellen. CAPICOM ist für die Verwendung in den Betriebssystemen verfügbar, die unter Run-Time Anforderungen angegeben sind. Für eine zukünftige Entwicklung empfiehlt es sich, die .NET Framework zum Implementieren von Sicherheitsfeatures zu verwenden. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.

CAPICOM 2.1.0.2 wird für die folgenden Betriebssysteme und Versionen unterstützt:

-   Windows Server 2003
-   Windows XP

CAPICOM ist als verteilbare Datei verfügbar, die von [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281)heruntergeladen werden kann.

Die Zertifikat Dienste erfordern die folgenden Versionen dieser Betriebssysteme:

-   Windows Server 2008 R2
-   WindowsServer 2008
-   Windows Server 2003

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                           | BESCHREIBUNG                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zur Kryptografie](about-cryptography.md)<br/>         | Wichtige kryptografiekonzepte und eine allgemeine Übersicht über die Kryptografietechnologien von Microsoft.<br/>                                                                                                                           |
| [Verwenden der Kryptografie](using-cryptography.md)<br/>         | Kryptografieprozesse, Prozeduren und Erweiterte Beispiele von C-und Visual Basic Programmen mithilfe von CryptoAPI-Funktionen und CAPICOM-Objekten.<br/>                                                                            |
| [Kryptografiereferenz](cryptography-reference.md)<br/> | Ausführliche Beschreibungen der Kryptografiefunktionen, Schnittstellen, Objekte, Strukturen und anderen Programmier Elemente von Microsoft. Enthält Referenz Beschreibungen der API für die Arbeit mit digitalen Zertifikaten.<br/> |



 

 

 




