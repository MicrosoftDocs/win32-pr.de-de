---
description: In diesem Thema werden die wichtigsten Überlegungen zur Programmierung beim Hinzufügen von MUI-Funktionen zu Ihren Anwendungen zusammengefasst.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Entwicklung von MUI-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867932"
---
# <a name="development-of-mui-applications"></a>Entwicklung von MUI-Anwendungen

In diesem Thema werden die wichtigsten Überlegungen zur Programmierung beim Hinzufügen von MUI-Funktionen zu Ihren Anwendungen zusammengefasst.

## <a name="requirements-for-a-mui-application"></a>Anforderungen an eine MUI-Anwendung

MUI-Funktionen werden nur auf die Lokalisierung einer vollständig globalisierte Anwendung angewendet, die mit einem Prozess namens Software Internationalisierung erstellt wurde. Das Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) bietet eine große Auswahl an verwandter Dokumentation, die Sie beim Entwerfen, entwickeln und Bereitstellen weltweit einsatzbereiter Anwendungen unterstützt. Mit diesen Dokumenten können Sie in Erwägung gezogen werden, wie sich die Merkmale unterschiedlicher Sprachen auf den Entwurf Ihrer Software auswirken können. Beachten Sie, dass das Portal auch ein umfassendes Archiv der Dr. International-Spalten enthält.

Ihre MUI-Anwendung kann unter jeder beliebigen Sprache oder Gebiets Schema Einstellung ausgeführt werden, und der Benutzer kann jede beliebige Sprache anfordern, für die die Anwendung Unterstützung bietet. Daher muss die Anwendung Benutzeroberflächen Text codieren, um die größtmögliche Vielfalt von Sprachen zu unterstützen. Der wichtigste Punkt, den Sie beachten müssen, ist die Verwendung von [Unicode](unicode.md) , um die gesamte Textverarbeitung zu verarbeiten. Weitere Informationen zur Globalisierung mithilfe von Unicode finden Sie im Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal).

## <a name="supported-programming-environments"></a>Unterstützte Programmierumgebungen

Sie können MUI-Funktionen zu einer globalisierten Win32 Forms-Anwendung oder-Konsolenanwendung hinzufügen, wie in diesem SDK beschrieben. Außerdem können Sie mit .NET Framework verwaltete Anwendungen erstellen, die mit MUI kompatibel sind. Weitere Informationen finden Sie unter [.net-Entwicklung](/previous-versions/ff361664(v=vs.100)).

## <a name="user-interface-language-settings"></a>Spracheinstellungen der Benutzeroberfläche

Wenn Sie Ihre MUI-Anwendung planen, müssen Sie zuerst die Sprachen für die Benutzeroberfläche und die Art der Darstellung für den Benutzer festlegen. Die Anwendung kann Sprachen auf eine der folgenden Arten unterstützen:

-   Befolgen Sie die Einstellungen der Systemsprache. Nehmen Sie an, dass die bevorzugten Benutzeroberflächen Sprachen und die bevorzugten Benutzeroberflächen Sprachen des Benutzers die Sprachen darstellen, die für den Benutzer verfügbar sind. Verwenden Sie den Fall Back Mechanismus des Ressourcen Laders für die Sprachauswahl.
-   Nehmen Sie anwendungsspezifische Spracheinstellungen vor. Unterstützen Sie bestimmte Sprachen, und stellen Sie dem Benutzer einen Auswahlmechanismus zur Verfügung.

## <a name="resource-creation"></a>Erstellen von Ressourcen

In diesem Abschnitt werden die Möglichkeiten beschrieben, die Benutzeroberflächen Sprachressourcen für die Anwendung zu erstellen. Weitere Informationen finden Sie unter [Vorbereiten von Ressourcen](preparing-resources.md).

> [!Note]  
> Bei Betriebssystemen vor Windows Vista erstellen Sie in der Regel statische und separat gepackte lokalisierte Anwendungen mit einer Sprache, die von den in den ausführbaren Dateien enthaltenen Ressourcen Abschnitten unterstützt werden. Dieser Implementierungstyp ist größtenteils veraltet, und es wird empfohlen, eine der anderen Verfahren zur Ressourcen Erstellung auszuwählen, die in diesem Abschnitt beschrieben werden, der für Windows Vista und höher unterstützt wird. Die Anwendung kann dann unter Verwendung von [**loadmuilibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)auf Betriebssystemen vor Windows Vista ausgeführt werden.

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Verwendung einer einzelnen Sprache in einer Ressourcen-DLL (MUI-Ressourcen Technologie)

Eine Standard-Satelliten-DLL-Ressourcen Implementierung wird von vielen Microsoft-Anwendungen verwendet. In diesem Fall wird eine ausführbare Kerndatei für die MUI-Anwendung verwendet, und für jede unterstützte Sprache wird eine Ressourcen-DLL erstellt. Die Verwendung einer Satelliten-DLL gilt für Anwendungen, die unter jedem Windows-Betriebssystem ausgeführt werden. Wie in der [MUI-Ressourcenverwaltung](mui-resource-management.md)beschrieben, unterstützt die MUI-Ressourcen Technologie eine Variation der Standard-Satelliten-DLL-Implementierung.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Verwendung mehrerer Sprachen in einer Ressourcen-DLL

Sie können auswählen, dass Sie eine ausführbare Datei für Ihre MUI-Anwendung und eine Ressourcen-DLL für die Ressourcen erstellen, die unterstützten Sprachen zugeordnet sind. Kopien desselben Ressourcen Bezeichners werden in der Ressourcen Datei der Basis Sprache (RC-Erweiterung) unter verschiedenen sprach Tags für alle unterstützten Sprachen definiert.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Verwendung eines Application-Specific-Ressourcenmechanismus

Sie können Ihre MUI-Anwendung für die Verwendung eines angepassten Ressourcenmechanismus planen. In diesem Fall behandelt die Anwendung das Laden von Ressourcen auf spezielle Weise.

## <a name="resource-localization"></a>Ressourcen Lokalisierung

Um die Sprachen der Benutzeroberfläche für Ihre MUI-Anwendung zu unterstützen, müssen Sie die Sprachressourcen lokalisiert haben. MUI unterstützt zwei Arten von Lokalisierung, wie in der folgenden Tabelle beschrieben.



| Lokalisierungs Typen       | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lokalisierung vor dem Build  | Anfordern der Lokalisierung vor dem entwickeln der Anwendungs-und sprachspezifischen Ressourcen. Die Ressourcen Datei für die Basis Sprache der unterstützten Benutzeroberflächen Sprachen wird für jede unterstützte Sprache kopiert und umbenannt, und die Kopien werden den Lokalisierern nach Bedarf bereitgestellt. |
| Lokalisierung nach dem Build | Anforderungs Lokalisierung nach dem Aufbau der ausführbaren Datei und der Ressourcen-DLL für Ihre Anwendung. In diesem Fall wird für jeden Lokalisierer eine Kopie der Ressourcen-DLL bereitgestellt.                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über mehrsprachige Benutzeroberfläche](about-multilingual-user-interface.md)
</dt> </dl>

 

 
