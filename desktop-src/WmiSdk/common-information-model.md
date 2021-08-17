---
description: Das Common Information Model (CIM) ist ein erweiterbares, objektorientiertes Datenmodell, das Informationen zu verschiedenen Teilen eines Unternehmens enthält.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Common Information Model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d095dfb7f05b7637ac027e6ea02eeba2e10e12845670aebd635e50e8c3265fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131642"
---
# <a name="common-information-model"></a>Common Information Model

Das Common Information Model (CIM) ist ein erweiterbares, objektorientiertes Datenmodell, das Informationen zu verschiedenen Teilen eines Unternehmens enthält. Cim [](https://www.dmtf.org/standards/cim) ist ein plattformübergreifender Standard, der von der Distributed Management Task Force[(DMTF)](https://www.dmtf.org/)verwaltet wird. Über WMI kann ein Entwickler mithilfe von CIM Klassen für Festplatten, Anwendungen, Netzwerkrouter und sogar für benutzerdefinierte Technologien wie etwa eine vernetzte Klimaanlage erstellen. Durch Anzeigen und Ändern einer CIM-Klasse kann ein Manager unterschiedliche Aspekte des Unternehmens steuern. So kann er beispielsweise eine CIM-Klasseninstanz für eine Desktop-Arbeitsstation abfragen. Anschließend kann er ein Skript ausführen, um die CIM-Arbeitsstationsinstanz zu ändern. Sämtliche Änderungen an der CIM-Klasseninstanz der Arbeitsstation werden von WMI in Änderungen an der eigentlichen Arbeitsstation umgewandelt.

Cim ist ein sprachunabhängiges Programmiermodell, das objektorientierte Techniken verwendet, um ein Unternehmen zu beschreiben. Mithilfe von drei Ebenen der Vererbung über- und untergeordneter Elemente kann CIM sowohl allgemeine als auch spezifische Aspekte eines Unternehmens beschreiben. Das CIM verwendet auch eine Technik namens "Zuordnung", um verschiedene Teile des Unternehmensmodells miteinander zu verknüpfen, und verwendet Schemas, um verschiedene Verwaltungsumgebungen zu unterscheiden.

Cim ist so konzipiert, dass eine konsistente Ansicht logischer und physischer Objekte in einer Verwaltungsumgebung dargestellt wird. Cim stellt verwaltete Objekte mithilfe eines objektorientierten Konstrukts dar, das als "Klasse" bezeichnet wird. Wie eine C++- oder COM-Klasse kann eine CIM-Klasse Eigenschaften enthalten, um Daten und Methoden zum Beschreiben des Verhaltens zu beschreiben. Wie ein Satz von COM-Klassen ist cim nicht an eine Plattform gebunden. WMI enthält jedoch eine Erweiterung des CIM, die die Microsoft Windows Betriebssystemplattformen beschreibt.

Cim definiert drei Klassenebenen:

-   Core

    Kernklassen stellen verwaltete Objekte dar, die für alle Verwaltungsbereiche gelten. Diese Klassen bieten ein grundlegendes Vokabular zum Analysieren und Beschreiben verwalteter Systeme. Die [**\_ \_ Klassen Parameters**](--parameters.md) und [**\_ \_ SystemSecurity**](--systemsecurity.md) sind Beispiele für Kernklassen.

-   Allgemein

    Allgemeine Klassen stellen verwaltete Objekte dar, die für bestimmte Verwaltungsbereiche gelten. Gängige Klassen sind jedoch unabhängig von einer bestimmten Implementierung oder Technologie. Allgemeine Klassen sind eine Erweiterung der Kernklassen. Die [**CIM \_ UnitaryComputerSystem-Klasse**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) ist ein Beispiel für eine allgemeine Klasse.

-   Erweitert

    Erweiterte Klassen stellen verwaltete Objekte dar, die technologiespezifische Ergänzungen zu den allgemeinen Klassen sind. Eine erweiterte Klasse gilt in der Regel für eine bestimmte Plattform, z. B. UNIX oder die Microsoft Win32-Umgebung. Die [**Win32 \_ ComputerSystem-Klasse**](/windows/desktop/CIMWin32Prov/win32-computersystem) ist ein Beispiel für eine erweiterte Klasse.

Ein Entwickler kann eine Klasse von einer anderen Klasse ableiten. Eine abgeleitete Klasse stellt einen Sonderfall der übergeordneten Klasse dar und erbt alle Eigenschaften und Methoden des übergeordneten Elements. [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) erbt beispielsweise von [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Vererbungsbeziehungen können mithilfe der Systemeigenschaften **\_ \_ Ableitung,** **\_ \_ Umbenennung** und **\_ \_ SuperKlasse** bestimmt werden. Die **\_ \_ Ableitungssystemeigenschaft** ist ein Array von Zeichenfolgen, die die gesamte Vererbungskette bis einschließlich der Stammklasse auflisten, die auch in **\_ \_ Dery** enthalten ist. Die **\_ \_ SuperClass-Systemeigenschaft** zeigt das unmittelbar übergeordnete Element der aktuellen Klasse an.

WMI unterstützt auch Zuordnungen. Eine Zuordnung ist eine Beziehung zwischen zwei oder mehr verschiedenen WMI-Klassen. Beispielsweise verfügt eine ausgeführte Arbeitsstation in der Regel über einen Prozessor. Die WMI-Zuordnungsklasse [Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) ordnet die Arbeitsstationsklasse [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) der Prozessorklasse [**Win32 \_ Processor**](/windows/desktop/CIMWin32Prov/win32-processor)zu. Eine Zuordnungsklasse muss jedoch nicht zwei abhängige Klassen miteinander verknüpfen. Tatsächlich besteht der Hauptzweck einer Zuordnungsklasse darin, Beziehungen zwischen Klassen anzuzeigen, die nicht notwendigerweise voneinander abhängig sind. Weitere Informationen finden Sie unter [Deklarieren einer Zuordnungsklasse.](declaring-an-association-class.md)

Schließlich unterstützt WMI das Konzept von Schemas. Im Kontext von WMI ist ein Schema eine Gruppe von Klassen, die eine bestimmte Verwaltungsumgebung beschreiben. Das Microsoft Windows Software Development Kit (SDK) verwendet zwei Schemas: das CIM-Schema und das Win32-Schema. Die CIM-Schemaklassennamen beginnen mit [CIM, \_](cimclas.md)und die Win32-Schemaklassennamen beginnen mit [**\_ Win32.**](/windows/desktop/CIMWin32Prov/win32-provider) Das CIM-Schema enthält die Definitionen für die Kernklassen und allgemeinen Klassen, während das Win32-Schema die Definitionen für die erweiterten Klassen enthält, die der Win32-Umgebung gemeinsam sind. Ein Drittanbieter kann jedoch eigene Schemas erstellen, um anbieterspezifische Anforderungen zu beschreiben. Da Schemas unendlich erweiterbar sind, kann ein Entwickler immer neue Klassen hinzufügen, um neue verwaltete Objekte in einer vorhandenen Umgebung zu beschreiben. Der Einfachheit halber entscheiden sich die meisten Anbieter jedoch dafür, Schemas zu erstellen, die Eigenschaften von den CIM- oder Win32-Schemas erben.

 

 
