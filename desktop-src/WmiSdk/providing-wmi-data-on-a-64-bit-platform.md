---
description: Skripts und Anwendungen, die für 32-Bit-Betriebssysteme geschrieben wurden, sollten weiterhin ordnungsgemäß ausgeführt werden.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527746"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform

Skripts und Anwendungen, die für 32-Bit-Betriebssysteme geschrieben wurden, sollten weiterhin ordnungsgemäß ausgeführt werden. Wenn Sie über einen vorhandenen 32-Bit-Anbieter verfügen, können Sie auswerten, ob Sie für eine parallele Operation eine 64-Bit-Version schreiben müssen. Im Allgemeinen sind beide Versionen nicht erforderlich, und die 64-Bit-Version kann sowohl lokale 32-Bit-als auch 64-Bit-und Remote Clients bedienen. Verwenden Sie für den 32-Bit-Anwendungs Kompatibilitätsmodus jedoch Ihren vorhandenen 32-Bit-WMI-Anbieter auf einem 64-Bit-System, das im Modus "32-Bit WOW64" ausgeführt wird.

In seltenen Fällen müssen sowohl der 32-Bit-als auch der 64-Bit-Anbieter parallel auf 64-Bit-Systemen ausgeführt werden. In diesem Fall ist die geeignete Version des Anbieters, die geladen wird, davon abhängig, ob der Aufrufer 32-Bit oder 64-Bit und lokal oder Remote ist. Ein Aufrufer, der die verbindungsobjektflags " **\_ \_ providerarchitecture** " und "Requirements **\_ \_ darchitecture**" verwendet, kann anfordern, dass WMI einen nicht standardmäßigen Anbieter lädt. Weitere Informationen finden Sie unter " [erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)".

In dem ungewöhnlichen Fall, dass Sie die 32-Bit-und 64-Bit-Anbieter parallel ausführen müssen, müssen Sie sicherstellen, dass die Installations-und Deinstallations Szenarien sorgfältig verarbeitet werden. Dies liegt daran, dass WMI nur über ein [*Repository*](gloss-w.md) verfügt und sowohl die 32-Bit-als auch die 64-Bit-Version von [**mofcomp.exe**](mofcomp.md) die Daten im selben Repository ablegen. Es gibt keinen Unterschied zwischen einer 32-Bit-oder einer 64-Bit. MOF-Datei. Die Neuinstallation einer Version des Anbieters wird nicht beeinträchtigt: die MOF-Dateien werden kompiliert und die Klassen werden im Repository gespeichert. Eine zweite Deinstallation, die einen Namespace löscht, kann jedoch den Betrieb des anderen Anbieters beeinträchtigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Anfordern von WMI-Daten auf einer 64-Bit-Plattform](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Bereitstellen von Daten für WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



