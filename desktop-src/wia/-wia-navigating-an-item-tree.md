---
description: Eine Anwendung navigiert durch die Elementstruktur eines Windows WIA-Geräts, um Bilder auf diesem Gerät zu suchen und auszuwählen. Mit dieser Technik wählt eine Anwendung ein Bild aus und erhält es, ohne dem Benutzer ein Dialogfeld anzuzeigen.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navigieren in einer Elementstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a8ef11fc534a621c31461df897c8cc81f987ef83163a1300b0e392ce4f190e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593020"
---
# <a name="navigating-an-item-tree"></a>Navigieren in einer Elementstruktur

Eine Anwendung navigiert durch die Elementstruktur eines Windows WIA-Geräts, um Bilder auf diesem Gerät zu suchen und auszuwählen. Mit dieser Technik wählt eine Anwendung ein Bild aus und erhält es, ohne dem Benutzer ein Dialogfeld anzuzeigen.

Ein WIA-Gerät wird als Stammelement in einer Struktur von [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) dargestellt. Die untergeordneten Elemente in der Struktur stellen Bilder für eine Kamera oder scannt für einen Scanner dar.

Nachdem ein WIA-Gerät ausgewählt wurde, ruft eine Anwendung die [**IWiaItem::EnumChildItems-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) der [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des Geräts auf, um die untergeordneten Elemente (bilder oder scannt) des Geräts aufzulisten. Anweisungen finden Sie unter [Auswählen eines Geräts.](-wia-selecting-a-device.md)

Die [**IWiaItem::EnumChildItems-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) erstellt ein Enumerationsobjekt für die untergeordneten Elemente des Geräts und gibt einen Zeiger auf die [**IEnumWiaItem-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) dieses Objekts zurück. Die Anwendung kann dann die Methoden der **IEnumWiaItem-Schnittstelle** verwenden, um Zeiger auf die Elemente in der Elementstruktur des Geräts abzurufen.

 

 



