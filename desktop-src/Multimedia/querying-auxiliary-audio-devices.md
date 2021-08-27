---
title: Abfragen von zusätzlichen Audiogeräten
description: Abfragen von zusätzlichen Audiogeräten
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- Waveform-Audio, Abfragen von zusätzlichen Audiogeräten
- Zusätzliche Audiodaten, Abfragen von Geräten
- Zusätzliche Audioschnittstelle
- Zusätzliche Audiogeräte,Abfragen
- Abfragen von zusätzlichen Audiogeräten
- Hilfsaudio, Schnittstelle
- Zusätzliche Audiodaten, Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a6d61634475c3b921428529df69113c921b8c5bff8d1a65d5b08931a670fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037570"
---
# <a name="querying-auxiliary-audio-devices"></a>Abfragen von zusätzlichen Audiogeräten

Nicht alle Multimediasysteme verfügen über zusätzliche Audiounterstützung. Sie können die [**Funktion auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) verwenden, um die Anzahl der steuerbaren Hilfsgeräte in einem System zu bestimmen.

Um Informationen zu einem bestimmten zusätzlichen Audiogerät zu erhalten, verwenden Sie die [**Funktion auxGetDevCaps.**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) Diese Funktion füllt eine [**AUXCAPS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) mit Informationen zu den Funktionen eines angegebenen Geräts auf. Diese Informationen umfassen die Hersteller- und Produkt-IDs, einen Produktnamen für das Gerät und die Gerätetreiber-Versionsnummer.

 

 