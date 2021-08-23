---
description: Die Geräteklasse "besent/in" besteht aus DEN SEQUENCErn, die für die Eingabe verwendet werden. Sie greifen auf diese Geräte mithilfe der IMK-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben sind.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: keyboard/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659950"
---
# <a name="midiin"></a>keyboard/in

Die Geräteklasse "besent/in" besteht aus DEN SEQUENCErn, die für die Eingabe verwendet werden. Sie greifen auf diese Geräte mithilfe der IMK-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben sind.

Die [**Funktionen lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügen diesen \_ zusätzlichen Member an:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Der **DeviceId-Member** ist der Bezeichner eines geschlossenen DANN-Geräts. Sie verwenden diesen Bezeichner in einem Aufruf der [**funktion "bezeichnerInOpen",**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) um das Gerät für die Eingabe zu öffnen. Sie können das resultierende Gerätehand handle verwenden, um DIE-Daten von der Linie oder dem Telefongerät zu erfassen.

Weitere Informationen zu den FUNKTIONS-Funktionen finden Sie unter [**Multimediafunktionen.**](../multimedia/multimedia-functions.md)

 

 
