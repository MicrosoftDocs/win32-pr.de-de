---
description: Das virtuelle BIOS ist ein Softwareimage, das in den RAM geladen wird, um einige der grundlegenden Aspekte eines Computersystems zu konfigurieren und zu starten. Es gibt ein BIOS-Element pro Computersystem, und dieses Element kann nicht ersetzt oder entfernt werden.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: BIOS-Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9605f28a23fc84b653ba5efe6c6e4be057eba48da81ddb777c7516d1317da6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813637"
---
# <a name="bios-classes"></a>BIOS-Klassen

Das virtuelle BIOS ist ein Softwareimage, das in den RAM geladen wird, um einige der grundlegenden Aspekte eines Computersystems zu konfigurieren und zu starten. Es gibt ein BIOS-Element pro Computersystem, und dieses Element kann nicht ersetzt oder entfernt werden. Daher gibt es keinen Ressourcenpool zum Hinzufügen neuer BIOS-Elemente zum virtuellen Computer. Das BIOS-Element verfügt auch nicht über eine eigene SettingData-Klasse, um die Einstellungen für das BIOS zu beschreiben. Einstellungen für das BIOS, z. B. Seriennummern, Startreihenfolge und Num-Sperrzustand, befinden sich in der [**Msvm \_ VirtualSystemSettingData-Klasse.**](msvm-virtualsystemsettingdata.md)

Im Folgenden sind Virtualisierungs-WMI-Klassen im Zusammenhang mit dem BIOS. Diese Klassen befinden sich im \\ \\ . \\ \\Stammvirtualisierungsnamespace.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                    | Beschreibung                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**Msvm \_ BIOSElement**](msvm-bioselement.md)<br/> | Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten.<br/> |
| [**Msvm \_ SystemBIOS**](msvm-systembios.md)<br/>   | Wird verwendet, um einem virtuellen Computer sein BIOS zuzuordnen.<br/>                                           |



 

 

 




