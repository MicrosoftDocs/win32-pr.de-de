---
description: 'Weitere Informationen: Einschränkungen des Skript Modells'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Einschränkungen des Skript Modells
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347778"
---
# <a name="limitations-of-the-scripting-model"></a>Einschränkungen des Skript Modells

> [!Note]  
> Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt. Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

Das WIA-Skript Modell (Windows Image Acquisition) stellt eine Teilmenge der WIA-Funktionalität zur Verfügung. In der folgenden Tabelle finden Sie Beschreibungen der Einschränkungen des Skript Modells. 

| WIA-Funktionalität               | Skript Modell Einschränkung                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterdrücken der Benutzeroberfläche  | Die Benutzeroberfläche zum Festlegen von Geräte/Übertragungseigenschaften kann nicht unterdrückt werden.                                                                                                                                                                                               |
| Festlegen von Eigenschaften              | Geräte-oder Element Eigenschaften können nicht festgelegt (geschrieben) werden.                                                                                                                                                                                                                        |
| Registrieren für Rückruf Ereignisse | Es können nur Benachrichtigungen für drei angegebene Ereignisse empfangen werden: [**ontransfercomplete**](-wia--iwiaevents-ontransfercomplete.md), [**ondeviceconnected**](-wia--iwiaevents-ondeviceconnected.md)und [**ondevicedevi.**](-wia--iwiaevents-ondevicedisconnected.md) |
| Behandlung von Fehlern                 | WIA-Fehler können nicht behandelt werden.                                                                                                                                                                                                                                                |



 

 

 
