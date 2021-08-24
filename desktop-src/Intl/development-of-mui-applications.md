---
description: In diesem Thema werden die wichtigsten Überlegungen zur Programmierung zusammengefasst, die beim Hinzufügen von MSI-Funktionen zu Ihren Anwendungen zu berücksichtigen sind.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Entwicklung von APPLICATIONS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cc647069577a2ff3b137573b85308aa66e685df2310c2ea01973d19d1dc0d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822770"
---
# <a name="development-of-mui-applications"></a>Entwicklung von APPLICATIONS

In diesem Thema werden die wichtigsten Überlegungen zur Programmierung zusammengefasst, die beim Hinzufügen von MSI-Funktionen zu Ihren Anwendungen zu berücksichtigen sind.

## <a name="requirements-for-a-mui-application"></a>Anforderungen für eineLIK-Anwendung

DIE FUNKTIONALITÄT WIRD nur auf die Lokalisierung einer vollständig globalisierten Anwendung angewendet, die mithilfe eines Prozesses namens Software internationalization erstellt wird. Das Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) bietet eine große Auswahl an zugehöriger Dokumentation, die Sie beim Entwerfen, Erstellen und Bereitstellen von weltweit einsatzbereiten Anwendungen unterstützt. Diese Dokumente helfen Ihnen zu überlegen, wie sich die Merkmale verschiedener menschlicher Sprachen auf den Entwurf Ihrer Software auswirken können. Beachten Sie, dass das Portal auch ein vollständiges Archiv von Dr. International-Spalten bereitstellt.

Ihre LANGUAGE-Anwendung kann unter einer beliebigen Sprach- oder Gebietsschemaeinstellung ausgeführt werden, und der Benutzer kann eine beliebige Sprache anfordern, für die die Anwendung Unterstützung enthält. Aus diesem Grund muss die Anwendung Benutzeroberflächentext codieren, um die größtmögliche Vielfalt von Sprachen zu unterstützen. Das Wichtigste, was Sie sich merken sollten, ist die Verwendung von [Unicode,](unicode.md) um die gesamte Textverarbeitung zu verarbeiten. Weitere Informationen zur Globalisierung mit Unicode finden Sie im Microsoft [Go Global Developer Center.](https://msdn.microsoft.com/goglobal)

## <a name="supported-programming-environments"></a>Unterstützte Programmierumgebungen

Sie können EINER globalisierten Win32 Forms-Anwendung oder Konsolenanwendung wie in diesem SDK beschrieben DIE FUNKTIONALITÄT hinzufügen. Darüber hinaus können Sie verwaltete Anwendungen mithilfe von .NET Framework erstellen, die mit DEM TON kompatibel ist. Weitere Informationen finden Sie unter [.NET-Entwicklung.](/previous-versions/ff361664(v=vs.100))

## <a name="user-interface-language-settings"></a>Benutzeroberfläche Language Einstellungen

Bei der Planung Ihrer ZIP-Anwendung müssen Sie sich zunächst für die Sprachen für die Benutzeroberfläche und die Möglichkeit entscheiden, sie dem Benutzer zu präsentieren. Die Anwendung kann Sprachen auf eine der folgenden Arten unterstützen:

-   Befolgen Sie die Einstellungen der Systemsprache. Angenommen, die vom Benutzer bevorzugten Benutzeroberflächensprachen und die vom System bevorzugten Benutzeroberflächensprachen stellen zusammen die sprachen dar, die dem Benutzer zur Verfügung stehen. Verwenden Sie den Fallbackmechanismus des Ressourcenladeprogramms für die Sprachauswahl.
-   Nehmen Sie anwendungsspezifische Spracheinstellungen vor. Unterstützen sie bestimmte Sprachen, und stellen Sie dem Benutzer einen Auswahlmechanismus zur Verfügung.

## <a name="resource-creation"></a>Ressourcenerstellung

In diesem Abschnitt werden die Möglichkeiten zum Erstellen der Benutzeroberflächen-Sprachressourcen für die Anwendung beschrieben. Weitere Informationen finden Sie unter [Vorbereiten von Ressourcen.](preparing-resources.md)

> [!Note]  
> Bei Betriebssystemen vor Windows Vista erstellen Sie im Allgemeinen statische und separat gepackte lokalisierte Einzelsprachanwendungen mit den Sprachen, die von ressourcenabschnitten unterstützt werden, die in den ausführbaren Dateien enthalten sind. Diese Art der Implementierung ist größtenteils veraltet, und Es wird empfohlen, eine der anderen In diesem Abschnitt beschriebenen Verfahren zum Erstellen von Ressourcen auszuwählen, die für Windows Vista und höher unterstützt werden. Die Anwendung kann dann mithilfe von [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)auf Betriebssystemen vor Windows Vista ausgeführt werden.

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Verwenden einer einzelnen Sprache in einer Ressourcen-DLL (RESOURCE Technology)

Eine Standardmäßige Implementierung von Satelliten-DLL-Ressourcen wird von vielen Microsoft-Anwendungen verwendet. In diesem Fall wird eine ausführbare Kerndatei für die WEBANWENDUNG verwendet, und für jede unterstützte Sprache wird eine Ressourcen-DLL erstellt. Die Verwendung einer Satelliten-DLL gilt für Anwendungen, die auf einem beliebigen Windows Betriebssystem ausgeführt werden. Wie in [DER RESSOURCENverwaltung](mui-resource-management.md)mit DEM THEMA BESCHRIEBEN, unterstützt die RESSOURCENtechnologie VON SICHE eine Variation der Standardmäßig-Satelliten-DLL-Implementierung.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Verwenden mehrerer Sprachen in einer Ressourcen-DLL

Sie können eine ausführbare Kerndatei für Ihre CSV-Anwendung und eine Ressourcen-DLL für die Ressourcen erstellen, die unterstützten Sprachen zugeordnet sind. Kopien desselben Ressourcenbezeichners werden in der Ressourcendatei der Basissprache (RC-Erweiterung) unter verschiedenen Sprachtags für alle unterstützten Sprachen definiert.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Verwenden eines Application-Specific-Ressourcenmechanismus

Sie können Ihre PLANS-Anwendung so planen, dass sie einen benutzerdefinierten Ressourcenmechanismus verwendet. In diesem Fall verarbeitet die Anwendung das Laden von Ressourcen auf spezielle Weise.

## <a name="resource-localization"></a>Ressourcenlokalisierung

Um die Sprachen der Benutzeroberfläche für Ihre LANGUAGE-Anwendung zu unterstützen, müssen Sie die Sprachressourcen lokalisiert haben. WIE in der folgenden Tabelle beschrieben, werden zwei Lokalisierungstypen unterstützt.



| Lokalisierungstyp       | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lokalisierung vor dem Build  | Fordern Sie die Lokalisierung an, bevor Sie die Anwendung und sprachspezifische Ressourcen erstellen. Die Ressourcendatei der Basissprache für die unterstützten Sprachen der Benutzeroberfläche wird für jede unterstützte Sprache kopiert und umbenannt, und die Kopien werden nach Bedarf für Diesser bereitgestellt. |
| Lokalisierung nach dem Build | Fordern Sie die Lokalisierung an, nachdem Sie die ausführbare Datei und die Ressourcen-DLL für Ihre Anwendung erstellt haben. In diesem Fall wird jedem Lokalisierer eine Kopie der Ressourcen-DLL bereitgestellt.                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu mehrsprachige Benutzeroberfläche](about-multilingual-user-interface.md)
</dt> </dl>

 

 
