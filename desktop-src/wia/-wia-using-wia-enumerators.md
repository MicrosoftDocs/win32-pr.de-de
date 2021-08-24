---
description: WIA bietet mehrere Schnittstellen zum Aufzählen verschiedener Funktionen, Eigenschaften und Informationen.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Verwenden von WIA-Enumeratoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b6e822d38c73171767d43afd416d09648bd6b82095b9408e2f17827751b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813470"
---
# <a name="using-wia-enumerators"></a>Verwenden von WIA-Enumeratoren

WIA bietet mehrere Schnittstellen zum Aufzählen verschiedener Funktionen, Eigenschaften und Informationen. Die Windows WIA-Enumerationsschnittstellen (Image Acquisition) sind alle spezifische Implementierungen der STANDARD-COMPONENT OBJECT MODEL-Enumerationsschnittstelle (COM). Weitere Informationen finden Sie unter [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

Die folgende Tabelle enthält Informationen zu den WIA-Enumerationsschnittstellen. 

| Schnittstelle                                                   | Abrufen eines Zeigers                                                                                                                                                                                    | Verwendung                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Rufen Sie [**eine IWiaItem::EnumDeviceCapabilities-**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) oder [**IWiaItem2::EnumDeviceCapabilities-Methode**](-wia-iwiaitem2-enumdevicecapabilities.md) eines WIA-Stammelements auf. | Aufzählen der Funktionen eines WIA-Hardwaregeräts, z. B. Gerätebefehle und Ereignisse.                                            |
| [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Rufen Sie [**die IWiaDevMgr::EnumDeviceInfo-**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) oder [**IWiaDevMgr2::EnumDeviceInfo-Methode**](-wia-iwiadevmgr2-enumdeviceinfo.md) auf.                                            | Enumeriert verfügbare WIA-Geräte und stellt Zeiger auf ihre [**IWiaPropertyStorage-Schnittstellen**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) bereit. |
| [**IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Rufen Sie [**eine IWiaDataTransfer::idtEnumWIA \_ FORMAT \_ INFO-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) eines Elements auf.                                                                              | Enumeriert alle Bildformatinformationen, die ein WIA-Element bietet.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Rufen Sie [**eine IWiaItem::EnumChildItems-**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) oder [**IWiaItem2::EnumChildItems-Methode**](-wia-iwiaitem2-enumchilditems.md) des WIA-Elements auf.                                          | Enumeriert die untergeordneten Elemente eines WIA-Elements, das entweder ein Gerät oder einen Ordner darstellt.                                                |



 

 

 
