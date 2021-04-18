---
description: In WMI ist eine Klasse ein Objekt, das einen Aspekt eines Unternehmens beschreibt, z. b. eine besondere Art von Laufwerk.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Erstellen einer WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351505"
---
# <a name="creating-a-wmi-class"></a>Erstellen einer WMI-Klasse

In WMI ist eine Klasse ein Objekt, das einen Aspekt eines Unternehmens beschreibt, z. b. eine besondere Art von Laufwerk. Nachdem Sie eine Klassendefinition erstellt haben, schreiben Sie die Anbieter-DLL, um Instanzen der Klasse, der Eigenschafts Daten und der Ausführungsmethoden bereitzustellen, die für die Klasse definiert wurden. Skripts und Anwendungen können dann Daten abrufen oder das Gerät steuern. Weitere Informationen finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).

> [!Note]  
> Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Anweisungs Präprozessoranweisung in der MOF-Datei.

 

## <a name="base-class"></a>Basisklasse

Eine Basisklasse stellt ein allgemeines Konzept dar. Die [**CIM- \_ cdromdrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) -Klasse stellt beispielsweise alle Arten von CD-ROM-Laufwerken in WMI dar und enthält allgemeine Eigenschaften, die alle Arten von CD-ROM-Laufwerken beschreiben. Weitere Informationen finden Sie unter [Erstellen einer Basisklasse](creating-a-base-class.md).

Eine abgeleitete Klasse erbt Eigenschaften und Methoden von einer anderen Klasse. Eine abgeleitete Klasse stellt in der Regel einen bestimmten Fall einer Basisklasse dar. Beispielsweise stellt die [**Win32 \_ cdromdrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) -Klasse ein CD-ROM-Laufwerk in einem Windows-System dar. Die **Win32 \_ cdromdrive** -Klasse basiert auf und erbt viele Eigenschaften von [**CIM \_ cdromdrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive). Allerdings kann **Win32 \_ cdromdrive**, wie andere abgeleitete Klassen, über zusätzliche Eigenschaften verfügen, die die abgeleitete Klasse eindeutig machen. Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md).

## <a name="properties-and-methods"></a>Eigenschaften und Methoden

Das Erstellen einer Klasse bedeutet, dass die Eigenschaften definiert werden, die diese Klasse beschreiben. Sie können auch Methoden definieren, die das von der-Klasse dargestellte Objekt bearbeiten.

Im Allgemeinen stellt eine Eigenschaft einen Aspekt des Objekts dar, z. b. eine Seriennummer für ein Gerät oder eine Größe in Byte für einen Prozess, während eine Methode eine Aktion darstellt, die den Zustand oder das Verhalten des Geräts oder der logischen Entität ändert.

Jede Klasse muss mindestens eine Schlüsseleigenschaft haben. Obwohl eine Klasse mehrere Schlüssel haben kann, können Sie keine Instanz einer Klasse mit mehr als 256 Schlüsseln erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
