---
description: 'Weitere Informationen zu: Einschränkungen des Skriptmodells'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Einschränkungen des Skriptmodells
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4a1b2dc25c1ea73fd9d793e4d3de1bff7c8193b04aadbe00796ca4a021791886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208062"
---
# <a name="limitations-of-the-scripting-model"></a>Einschränkungen des Skriptmodells

> [!Note]  
> Dieses Skriptsystem wurde durch Windows Image Acquisition (WIA) Automation Layer ersetzt. Weitere Informationen finden Sie [unter Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Das WIA-Skriptmodell (Windows Image Acquisition) macht eine Teilmenge der WIA-Funktionalität verfügbar. Die folgende Tabelle enthält Beschreibungen der Einschränkungen des Skriptmodells. 

| WIA-Funktionalität               | Einschränkung des Skriptmodells                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterdrücken der Benutzeroberfläche  | Die Benutzeroberfläche zum Festlegen von Geräte-/Übertragungseigenschaften kann nicht unterdrückt werden.                                                                                                                                                                                               |
| Festlegen von Eigenschaften              | Geräte- oder Elementeigenschaften können nicht festgelegt (geschrieben) werden.                                                                                                                                                                                                                        |
| Registrieren für Rückrufereignisse | Kann nur Benachrichtigungen für drei angegebene Ereignisse empfangen: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)und [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md). |
| Behandlung von Fehlern                 | WIA-Fehler können nicht behandelt werden.                                                                                                                                                                                                                                                |



 

 

 
