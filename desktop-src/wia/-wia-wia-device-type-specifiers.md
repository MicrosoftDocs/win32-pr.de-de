---
description: Windows WiA-Gerätetypspezifizierer (Image Acquisition, Bilderfassung) sind Konstanten, die den Gerätetyp angeben, der an den Computer eines Benutzers angefügt ist.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: WIA-Gerätetypspezifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdefac4672b46fea7a7dad021fa9ebec710b3b77eabb7a1f7cac405b8e7e519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056970"
---
# <a name="wia-device-type-specifiers"></a>WIA-Gerätetypspezifizierer

Windows WiA-Gerätetypspezifizierer (Image Acquisition, Bilderfassung) sind Konstanten, die den Gerätetyp angeben, der an den Computer eines Benutzers angefügt ist. Verwenden Sie das MAKRO GET \_ STIDEVICE \_ TYPE, um diese Werte aus der WIA-Gerätetypeigenschaft zu erhalten. Im Folgenden finden Sie gültige WIA-Gerätetypspezifizierer: 

| Gerätetyp                 | Bedeutung                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Generisches WIA-Gerät. Während der Geräteenumeration wird diese Konstante verwendet, um alle WIA-Geräte aufzählen.                         |
| StiDeviceTypeDigitalCamera  | Das Gerät ist eine Kamera. *Dieser Spezifizierer wird von Windows* Vista *und höher nicht unterstützt.*                                     |
| StiDeviceTypeScanner        | Das Gerät ist ein Scanner.                                                                                                    |
| StiDeviceTypeStreamingVideo | Das Gerät enthält Streamingvideos. *Dieser Bezeichner wird von Server* 2003 Windows Server 2003, Windows Vista oder höher nicht *unterstützt.* |



 

 

 



