---
description: Die Wave/in-Geräteklasse besteht aus Audiogeräten für eine Wave-Audioeingabe auf niedriger Ebene.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: Wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217750"
---
# <a name="wavein"></a>Wave/in

Die Wave/in-Geräteklasse besteht aus Audiogeräten für eine Wave-Audioeingabe auf niedriger Ebene. Sie greifen auf diese Geräte mithilfe der Wave-Funktionen zu, die im Platform Software Development Kit (SDK) beschrieben werden. Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ automatedvoice unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.

Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Der Member " **enviceid** " ist der Bezeichner eines geschlossenen Audiogeräts. Sie verwenden diesen Bezeichner in einem Aufrufe der [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion, um das Gerät für die Eingabe zu öffnen. Sie können das resultierende Geräte Handle verwenden, um digitalisierte Audiodaten von der Zeile oder dem Telefongerät aufzuzeichnen.

Obwohl eine "Wave"-Geräteklasse auch für Wellen Audiogeräte auf niedriger Ebene vorhanden ist, sollten Sie immer die Wave/in-Geräteklasse für Wellen Eingaben auf niedriger Ebene verwenden.

Weitere Informationen zu den Wave-Funktionen finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).

 

 
