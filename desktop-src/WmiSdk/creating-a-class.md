---
description: In WMI ist eine Klasse ein Objekt, das einen Aspekt eines Unternehmens beschreibt, z. B. einen speziellen Datenträgertyp.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Erstellen einer WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2db62f1f0d14035f7bcc3fd74f8bbbfbacf08cb0dbf139b06c9870b7039e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612560"
---
# <a name="creating-a-wmi-class"></a>Erstellen einer WMI-Klasse

In WMI ist eine Klasse ein Objekt, das einen Aspekt eines Unternehmens beschreibt, z. B. einen speziellen Datenträgertyp. Nachdem Sie eine Klassendefinition erstellt haben, schreiben Sie die Anbieter-DLL, um Instanzen der Klasse, Eigenschaftendaten und für die Klasse definierte Methoden auszuführen. Skripts und Anwendungen können dann Daten abrufen oder das Gerät steuern. Weitere Informationen finden Sie unter [Entwickeln eines WMI-Anbieters.](developing-a-wmi-provider.md)

> [!Note]  
> Um sicherzustellen, dass alle WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wiederhergestellt werden, wenn WMI einen Fehler auftrat und neu gestartet wird, verwenden Sie die [**\# Präprozessoranweisung pragma autorecover**](pragma-autorecover.md) statement in Ihrer MOF-Datei.

 

## <a name="base-class"></a>Basisklasse

Eine Basisklasse stellt ein allgemeines Konzept dar. Die CIM [**\_ C CIM-Klasse stellt**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) beispielsweise alle Typen von CD-ROM-Laufwerken in WMI dar und enthält allgemeine Eigenschaften, die alle Arten von CD-ROM-Laufwerken beschreiben. Weitere Informationen finden Sie unter [Erstellen einer Basisklasse.](creating-a-base-class.md)

Eine abgeleitete Klasse erbt Eigenschaften und Methoden von einer anderen Klasse. Eine abgeleitete Klasse stellt normalerweise einen bestimmten Fall einer Basisklasse dar. Beispielsweise stellt die [**Win32 \_ CLASSDrive-Klasse**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) ein CD-ROM-Laufwerk auf einem Windows dar. Die **Win32 \_ C CMDLETDrive-Klasse** basiert auf und erbt viele Eigenschaften von [**CIM C CIM C \_ CIMDrive.**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) **Win32 \_ CKATDrive** kann jedoch wie andere abgeleitete Klassen über zusätzliche Eigenschaften verfügen, die die abgeleitete Klasse eindeutig machen. Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse.](creating-a-derived-class.md)

## <a name="properties-and-methods"></a>Eigenschaften und Methoden

Das Erstellen einer Klasse bedeutet, die Eigenschaften zu definieren, die diese Klasse beschreiben. Sie können auch Methoden definieren, die das durch die -Klasse dargestellte Objekt bearbeiten.

Im Allgemeinen stellt eine Eigenschaft einen Aspekt des Objekts dar, z. B. eine Seriennummer für ein Gerät oder eine Größe in Bytes für einen Prozess, während eine Methode eine Aktion darstellt, die den Zustand oder das Verhalten des Geräts oder der logischen Entität ändert.

Jede Klasse muss mindestens eine Schlüsseleigenschaft haben. Obwohl eine Klasse mehrere Schlüssel haben kann, können Sie keine Instanz einer Klasse mit mehr als 256 Schlüsseln erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen Managed Object Format -Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
