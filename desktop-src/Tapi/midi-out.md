---
description: Die Geräteklasse "keyboard/out" besteht aus DEN FÜR die Ausgabe verwendeten SEQUENCE-Sequencern. Sie greifen auf diese Geräte mithilfe der IMK-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben sind.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: ein- und aus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c0199cc7918ab9aeacb3210b6f98d5ff03fc3bca90624bee00d864727ae0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518610"
---
# <a name="midiout"></a>ein- und aus

Die Geräteklasse "keyboard/out" besteht aus DEN FÜR die Ausgabe verwendeten SEQUENCE-Sequencern. Sie greifen auf diese Geräte mithilfe der IMK-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben sind.

Die [**Funktionen lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**VARSTRING-Struktur**](/windows/desktop/api/Tapi/ns-tapi-varstring) aus, legen den **dwStringFormat-Member** auf den STRINGFORMAT BINARY-Wert und fügen diesen \_ zusätzlichen Member an:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Der **DeviceId-Member** ist der Bezeichner eines geschlossenen DANN-Geräts. Sie verwenden diesen Bezeichner in einem Aufruf der [**Funktion "bezeichnerOutOpen",**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) um das Gerät für die Ausgabe zu öffnen. Sie können das resultierende Gerätehand handle verwenden, um DIE Daten auf der Linie oder dem Telefon wiedergeben.

Weitere Informationen zu denFUNKTIONSfunktionen finden Sie unter [**Multimediafunktionen**](../multimedia/multimedia-functions.md).

 

 
