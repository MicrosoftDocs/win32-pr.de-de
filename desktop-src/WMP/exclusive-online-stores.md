---
title: Exklusive Online Stores
description: Exklusive Online Stores
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player Online Stores, exklusiv
- Online Stores, exklusiv
- Geben Sie 1 Online Stores ein, exklusiv
- Typ 2 Online Stores, exklusiv
- exklusive Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338041"
---
# <a name="exclusive-online-stores"></a>Exklusive Online Stores

Bei Windows Media Player 11 kann eine Anwendung, die das Player-Steuerelement Remote einbettet, einen exklusiven Online Store angeben. In diesem Fall ist der Dienst-Selector in Windows-Media Player deaktiviert, und nur der angegebene Onlinespeicher ist für den Benutzer verfügbar. Außerdem übernimmt Windows Media Player die durch das **Color** -Element des exklusiven Online Store-Dokuments angegebene Farbe.

Um einen exklusiven Online Store anzugeben, muss eine Anwendung exclusiveservice:*keyName* an das Ende der Zeichenfolge anfügen, die von [iwmpremotemediaservices:: getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)zurückgegeben wird. Angenommen, Proseware ist der Schlüssel Name, der einem bestimmten Online Store zugewiesen wird. Wenn **getservicetype** die Zeichenfolge "Remote exclusiveservice: Proseware" zurückgibt, ist Proseware der einzige Online Shop, der im Remote Embedded Player-Steuerelement verfügbar ist.

Eine Anwendung kann Windows Media Player nur dann auf einen exklusiven Online Store beschränken, wenn Windows Media Player nicht bereits ausgeführt wird, wenn die Anwendung gestartet wird. Die Anwendung ist dafür verantwortlich, den Benutzer darüber zu informieren, dass Sie Windows Media Player schließen muss, bevor die Anwendung ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




