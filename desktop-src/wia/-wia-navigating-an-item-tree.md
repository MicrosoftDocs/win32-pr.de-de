---
description: Eine Anwendung navigiert die Elementstruktur eines Windows-Abbild Erwerbs (WIA), um Abbilder auf diesem Gerät zu suchen und auszuwählen. Mit dieser Technik wählt eine Anwendung ein Bild aus und ruft ein Bild ab, ohne dem Benutzer ein Dialogfeld zu präsentieren.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navigieren in einer Elementstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526432"
---
# <a name="navigating-an-item-tree"></a>Navigieren in einer Elementstruktur

Eine Anwendung navigiert die Elementstruktur eines Windows-Abbild Erwerbs (WIA), um Abbilder auf diesem Gerät zu suchen und auszuwählen. Mit dieser Technik wählt eine Anwendung ein Bild aus und ruft ein Bild ab, ohne dem Benutzer ein Dialogfeld zu präsentieren.

Ein WIA-Gerät wird als Stamm Element in einer Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten dargestellt. Die untergeordneten Elemente in der Struktur stellen Bilder für eine Kamera oder Scan Betten für einen Scanner dar.

Nach dem Auswählen eines WIA-Geräts wird von einer Anwendung die [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) -Methode der [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Geräts aufgerufen, um die untergeordneten Elemente (die Bilder oder Scan Betten) des Geräts aufzuzählen. Anweisungen hierzu finden Sie unter [Auswählen eines Geräts](-wia-selecting-a-device.md).

Die [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) -Methode erstellt ein Enumerationsobjekt für die untergeordneten Elemente des Geräts und gibt einen Zeiger auf die [**ienumwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) -Schnittstelle dieses Objekts zurück. Die Anwendung kann dann die Methoden der **ienumwiaitem** -Schnittstelle verwenden, um Zeiger auf die Elemente in der Elementstruktur des Geräts zu erhalten.

 

 



