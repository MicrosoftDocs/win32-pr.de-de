---
description: Das virtuelle BIOS ist ein Software Abbild, das in den RAM geladen wird, um einige der grundlegenden Aspekte von zu konfigurieren und ein Computersystem zu starten. Es gibt ein BIOS-Element pro Computersystem, und dieses Element kann nicht ersetzt oder entfernt werden.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: BIOS-Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959804"
---
# <a name="bios-classes"></a>BIOS-Klassen

Das virtuelle BIOS ist ein Software Abbild, das in den RAM geladen wird, um einige der grundlegenden Aspekte von zu konfigurieren und ein Computersystem zu starten. Es gibt ein BIOS-Element pro Computersystem, und dieses Element kann nicht ersetzt oder entfernt werden. Folglich gibt es keinen Ressourcenpool zum Hinzufügen neuer BIOS-Elemente zum virtuellen Computer. Das BIOS-Element verfügt auch nicht über eine eigene SettingData-Klasse, um die Einstellungen für das BIOS zu beschreiben. Die Einstellungen für das BIOS (z. b. Seriennummern, Start Reihenfolge und Num-Sperr Status) finden Sie in der Klasse " [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) ".

Im folgenden finden Sie WMI-Klassen für die Virtualisierung im Zusammenhang mit dem BIOS. Diese Klassen befinden sich im \\ \\ . \\ \\Namespace für die stammvirtualisierung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                    | BESCHREIBUNG                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**MSVM- \_ bioselements**](msvm-bioselement.md)<br/> | Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten.<br/> |
| [**MSVM- \_ Systembios**](msvm-systembios.md)<br/>   | Wird verwendet, um dem BIOS eine virtuelle Maschine zuzuordnen.<br/>                                           |



 

 

 




