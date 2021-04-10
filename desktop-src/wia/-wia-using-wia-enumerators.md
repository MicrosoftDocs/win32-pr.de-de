---
description: WIA stellt mehrere Schnittstellen zum Auflisten verschiedener Funktionen, Eigenschaften und Informationen bereit.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Verwenden von WIA-Enumeratoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee42f99718cb36071b828e87e3a71de6d70ab5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214645"
---
# <a name="using-wia-enumerators"></a>Verwenden von WIA-Enumeratoren

WIA stellt mehrere Schnittstellen zum Auflisten verschiedener Funktionen, Eigenschaften und Informationen bereit. Bei den enumerationsschnittstellen der Windows-Abbild Erfassung (WIA) handelt es sich um spezifische Implementierungen der Standard-Component Object Model (com)-Enumerationsschnittstelle. Weitere Informationen finden Sie unter [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

In der folgenden Tabelle finden Sie Informationen zu den WIA-enumerationsschnittstellen. 

| Schnittstelle                                                   | Abrufen eines Zeigers                                                                                                                                                                                    | Verwendung                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**Ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Aufrufen der [**iwiaitem:: enumdevicecapabili-**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) Methode oder der [**IWiaItem2:: enumdevicecapabili-**](-wia-iwiaitem2-enumdevicecapabilities.md) Methode eines WIA-Stamm Elements. | Listet die Funktionen eines WIA-Hardware Geräts auf, z. b. Geräte Befehle und Ereignisse.                                            |
| [**Ienumwia-Entwicklungs \_ \_ Informationen**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Nennen Sie die [**iwiadevmgr:: enumdeviceinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) -Methode oder die [**IWiaDevMgr2:: enumdeviceinfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) -Methode.                                            | Listet die verfügbaren WIA-Geräte auf und stellt Zeiger auf Ihre [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstellen bereit. |
| [**Ienumwia- \_ Format \_ Informationen**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Ruft eine [**iwiadatatransfer:: idtenrewia- \_ Format \_ Info**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) Methode eines Elements auf.                                                                              | Listet alle Bildformat Informationen auf, die ein WIA-Element bereitstellt.                                                                    |
| [**Ienumwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Aufrufen der [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) -Methode oder der [**IWiaItem2:: enumchilditems**](-wia-iwiaitem2-enumchilditems.md) -Methode des WIA-Elements.                                          | Listet die untergeordneten Elemente eines WIA-Elements auf, das entweder ein Gerät oder einen Ordner darstellt.                                                |



 

 

 
