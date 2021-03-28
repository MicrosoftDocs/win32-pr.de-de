---
title: Gerätetreiber Informationen
description: Gerätetreiber und-Module sind insofern ähnlich, als beide auf PE-Dateien basieren.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036586"
---
# <a name="device-driver-information"></a>Gerätetreiber Informationen

Gerätetreiber und-Module sind insofern ähnlich, als beide auf PE-Dateien basieren. Obwohl jeder Prozess über eine eigene private Liste geladener Module verfügt, verfügen Gerätetreiber über Module, die für das System Global sind. Daher verfügt PSAPI über bestimmte Funktionen zum Abrufen der Liste der Gerätetreiber und ihrer Namen.

Sie können die Lade Adresse für jeden Gerätetreiber abrufen, indem Sie die [**enumdevicedrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) -Funktion aufrufen. Diese Funktion füllt ein Array von **LPVOID** -Werten mit den Lade Adressen aller Gerätetreiber im System.

Die [**getdevicedriverbasename**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) -Funktion nimmt eine Treiber Lade Adresse als Eingabe an und füllt einen Puffer mit dem Basisnamen des Treibers (z. b. Win32k.sys) aus. Die zugehörige Funktion [**getdevicedriverfilename**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea)übernimmt dieselben Parameter und gibt den Pfad zum Gerätetreiber zurück (z. b. C: \\ Windows \\ system32 \\Win32k.sys).

 

 




