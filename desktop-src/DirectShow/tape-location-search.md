---
description: Band Speicherort Suche
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Band Speicherort Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352634"
---
# <a name="tape-location-search"></a>Band Speicherort Suche

Die DV-Geräte unterstützen zwar einen Befehl für die Suche nach Zeit Code oder mit der absoluten Spur Nummer (ATN), der msdv-Treiber verfügt jedoch nicht über eine standardmäßige geräteunabhängige Methode, um auf diese Funktionen zuzugreifen. Die einzige Möglichkeit besteht darin, einen unformatierten AV/c-Befehl an den Treiber zu senden, wie im Thema [ausgeben von unformatierten AV/c-Befehlen](issuing-raw-av-c-commands.md)beschrieben.

Der UVC-Treiber unterstützt einen Eigenschaften Satz für die Suche nach bandorten. Um einen Suchbefehl zu senden, verwenden Sie die " **ikscontrol** "-Schnittstelle, und legen Sie die Eigenschaft "propsetid \_ \_ Die Verwendung eines Eigenschaften Satzes ist sicherer als das Senden von unformatierten AV/c-Befehlen an das Gerät, da der Filter durch die AV/c-Befehle umgangen und direkt zum Gerätetreiber geleitet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> <dt>

[Eigenschaften Satz für externen Geräte Transport](external-device-transport-property-set.md)
</dt> </dl>

 

 



