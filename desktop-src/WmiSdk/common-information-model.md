---
description: Das Common Information Model (CIM) ist ein erweiterbares, objektorientiertes Datenmodell, das Informationen zu verschiedenen Teilen eines Unternehmens enthält.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Common Information Model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e4e2dc06e03a1f19b5b47ba0b94d7a866a5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042685"
---
# <a name="common-information-model"></a>Common Information Model

Das Common Information Model (CIM) ist ein erweiterbares, objektorientiertes Datenmodell, das Informationen zu verschiedenen Teilen eines Unternehmens enthält. Der [CIM](https://www.dmtf.org/standards/cim) ist ein plattformübergreifender Standard, der von der verteilten Verwaltungs Task Force ([DMTF](https://www.dmtf.org/)) verwaltet wird. Über WMI kann ein Entwickler mithilfe von CIM Klassen für Festplatten, Anwendungen, Netzwerkrouter und sogar für benutzerdefinierte Technologien wie etwa eine vernetzte Klimaanlage erstellen. Durch Anzeigen und Ändern einer CIM-Klasse kann ein Manager unterschiedliche Aspekte des Unternehmens steuern. So kann er beispielsweise eine CIM-Klasseninstanz für eine Desktop-Arbeitsstation abfragen. Anschließend kann er ein Skript ausführen, um die CIM-Arbeitsstationsinstanz zu ändern. Sämtliche Änderungen an der CIM-Klasseninstanz der Arbeitsstation werden von WMI in Änderungen an der eigentlichen Arbeitsstation umgewandelt.

Der CIM ist ein sprachunabhängiges Programmiermodell, das objektorientierte Techniken verwendet, um ein Unternehmen zu beschreiben. Mit drei Ebenen der über-/unterordnungshiervererbung kann der CIM sowohl allgemeine als auch bestimmte Aspekte eines Unternehmens beschreiben. Der CIM verwendet auch eine Technik namens "Association", um verschiedene Teile des Unternehmensmodells miteinander zu verknüpfen, und verwendet Schemas, um unterschiedliche Verwaltungs Umgebungen zu unterscheiden.

Der CIM ist darauf ausgelegt, eine konsistente Ansicht logischer und physischer Objekte in einer Verwaltungs Umgebung darzustellen. Der CIM stellt verwaltete Objekte mit einem objektorientierten Konstrukt dar, das als "Klasse" bezeichnet wird. Wie eine C++-oder com-Klasse kann eine CIM-Klasse Eigenschaften enthalten, um Daten und Methoden zu beschreiben, um das Verhalten zu beschreiben. Wie bei einem Satz von COM-Klassen ist der CIM nicht an eine beliebige Plattform gebunden. WMI enthält jedoch eine Erweiterung für den CIM, in der die Microsoft Windows-Betriebssystemplattformen beschrieben werden.

Der CIM definiert drei Ebenen von Klassen:

-   Kernspeicher

    Kernklassen stellen verwaltete Objekte dar, die für alle Verwaltungsbereiche gelten. Diese Klassen stellen ein einfaches Vokabular zum Analysieren und beschreiben verwalteter Systeme bereit. Die [**\_ \_ Parameter**](--parameters.md) und die [**\_ \_ System Security**](--systemsecurity.md) -Klassen sind Beispiele für Kernklassen.

-   Allgemein

    Allgemeine Klassen stellen verwaltete Objekte dar, die für bestimmte Verwaltungsbereiche gelten. Allgemeine Klassen sind jedoch unabhängig von einer bestimmten Implementierung oder Technologie. Allgemeine Klassen sind eine Erweiterung der-Kernklassen. Die [**CIM \_ unitarycomputersystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) -Klasse ist ein Beispiel für eine gemeinsame Klasse.

-   Erweitert

    Erweiterte Klassen stellen verwaltete Objekte dar, bei denen es sich um technologiespezifische Ergänzungen der allgemeinen Klassen handelt. Eine erweiterte Klasse gilt in der Regel für eine bestimmte Plattform, z. b. UNIX oder die Microsoft Win32-Umgebung. Die [**Win32- \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) -Klasse ist ein Beispiel für eine erweiterte Klasse.

Ein Entwickler kann eine Klasse von einer anderen Klasse ableiten. Eine abgeleitete Klasse stellt einen Sonderfall der übergeordneten Klasse dar und erbt alle Eigenschaften und Methoden der übergeordneten Klasse. Beispielsweise erbt [**Win32 \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) von [**CIM \_ unitarycomputersystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Vererbungs Beziehungen können mithilfe der Systemeigenschaften **\_ \_ Ableitung**, der **\_ \_ Dynastie** und der über **\_ \_ geordneten Klasse** bestimmt werden. Die **\_ \_ abderivationsystemeigenschaft** ist ein Array von Zeichen folgen, das die gesamte Vererbungs Kette bis einschließlich der Stamm Klasse auflistet, die ebenfalls in der **\_ \_ Dynastie** enthalten ist. Die System Eigenschaft **\_ \_ Superclass** zeigt das unmittelbar übergeordnete Element der aktuellen Klasse an.

WMI unterstützt auch Zuordnungen. Eine Zuordnung ist eine Beziehung zwischen zwei oder mehr unterschiedlichen WMI-Klassen. Beispielsweise verfügt eine Arbeitsstation in der Regel über einen Prozessor. In der WMI-Zuordnungs Klasse Win32 [ \_ computersystemprocessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) wird die Arbeitsstations Klasse [**Win32 \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) mit dem [**Win32- \_ Prozessor**](/windows/desktop/CIMWin32Prov/win32-processor)der Prozessor Klasse verknüpft. Allerdings muss eine Association-Klasse nicht zwei abhängige Klassen miteinander verknüpfen. Der primäre Zweck einer Zuordnungs Klasse besteht darin, Beziehungen zwischen Klassen, die nicht notwendigerweise voneinander abhängen, anzuzeigen. Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).

Und schließlich unterstützt WMI das Konzept von Schemas. Im Kontext von WMI ist ein Schema eine Gruppe von Klassen, die eine bestimmte Verwaltungs Umgebung beschreiben. Das Microsoft Windows Software Development Kit (SDK) verwendet zwei Schemas: das CIM-Schema und das Win32-Schema. Die CIM-Schema Klassennamen beginnen [mit \_ CIM](cimclas.md), und die Win32-Schema Klassennamen beginnen mit [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-provider). Das CIM-Schema enthält die Definitionen für die Kern-und allgemeine Klassen, während das Win32-Schema die Definitionen für die erweiterten Klassen enthält, die für die Win32-Umgebung üblich sind. Ein Drittanbieter kann jedoch eigene Schemas erstellen, um herstellerspezifische Anforderungen zu beschreiben. Da Schemas so konzipiert sind, dass Sie unendlich erweiterbar sind, kann ein Entwickler immer neue Klassen hinzufügen, um neue verwaltete Objekte in einer vorhandenen Umgebung zu beschreiben. Der Einfachheit halber entscheiden sich die meisten Anbieter jedoch für die Erstellung von Schemas, die Eigenschaften von den CIM-oder Win32-Schemas erben.

 

 
