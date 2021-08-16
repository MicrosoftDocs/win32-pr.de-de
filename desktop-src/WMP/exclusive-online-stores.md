---
title: Exklusive Onlineshops
description: Exklusive Onlineshops
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player,exklusiv
- Onlineshops,exklusiv
- Typ 1 Onlineshops,exklusiv
- Typ 2 Onlineshops,exklusiv
- Exklusive Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d199c47a201743ca56f9f9f199b5202bbdbe5fb320628afc5052b0ca8b969c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650090"
---
# <a name="exclusive-online-stores"></a>Exklusive Onlineshops

Mit Windows Media Player 11 kann eine Anwendung, die das Player-Steuerelement remote einbettet, einen exklusiven Onlineshop angeben. In diesem Fall ist die Dienstauswahl in Windows Media Player deaktiviert, und nur der angegebene Onlineshop ist für den Benutzer verfügbar. Außerdem übernimmt Windows Media Player farbe, die durch das **Color-Element** des ServiceInfo-Dokuments des exklusiven Onlineshops angegeben wird.

Um einen exklusiven Onlineshop anzugeben, muss eine Anwendung ExclusiveService:*keyname* an das Ende der Zeichenfolge anfügen, die sie von [IWMPRemoteMediaServices::GetServiceType zurückgibt.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype) Angenommen, Proseware ist der Schlüsselname, der einem bestimmten Onlineshop gegeben wird. Wenn **GetServiceType** die Zeichenfolge "Remote ExclusiveService:Proseware" zurückgibt, ist Proseware der einzige Onlineshop, der im remote eingebetteten Player-Steuerelement verfügbar ist.

Eine Anwendung kann Windows Media Player auf einen exklusiven Onlineshop beschränken, wenn Windows Media Player beim Start der Anwendung noch nicht ausgeführt wird. Es liegt in der Verantwortung der Anwendung, den Benutzer darüber zu informieren, dass er die Windows Media Player vor dem Ausführen der Anwendung schließen muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




