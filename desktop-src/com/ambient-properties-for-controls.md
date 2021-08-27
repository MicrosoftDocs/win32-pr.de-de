---
title: Umgebungseigenschaften für Steuerelemente
description: Umgebungseigenschaften für Steuerelemente
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421a643873e818d8f5c0e006b4bb9049c1230c5f4e18525cdf7ed2b4175797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994060"
---
# <a name="ambient-properties-for-controls"></a>Umgebungseigenschaften für Steuerelemente

Wenn ein Steuerelement umgebungseigenschaften überhaupt unterstützt, muss es mindestens die Werte der folgenden Umgebungseigenschaften unter den in der folgenden Tabelle unter Verwendung der Standarddispiden angegebenen Bedingungen achten.



| Ambient-Eigenschaft            | Dispid          | Kommentar/Bedingungen für die Verwendung                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Wenn das Locale für das Steuerelement von Bedeutung ist, z. B. für die Textausgabe<br/>                                                                                                                                                                                                                  |
| Usermode <br/>        | -709<br/> | Wenn sich das Steuerelement im Benutzermodus (Entwurfsmodus) und im Ausführungsmodus anders verhält<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Wenn das Steuerelement auf Benutzeroberflächenereignisse reagiert, sollte es diese Ambient-Eigenschaft verwenden.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Wenn das Steuerelement die größenbasierte Größenverfingung von sich selbst unterstützt<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Wenn das Steuerelement die aktivierung und die Aktivierung der Benutzeroberfläche unterstützt<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Nur wenn das Steuerelement als OLEMISC ACTSLIKEBUTTON gekennzeichnet ist (d. h., es wird Unterstützung für Mnemonische Tastaturen bereitgestellt, daher müssen \_ [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) und [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) implementiert werden).<br/> |



 

Wie zuvor beschrieben, erfordert die Verwendung von Ambients sowohl [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (mindestens [**für OnAmbientPropertyChange)**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) als auch [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) [**(für SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) und [**GetClientSite).**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)

Das OLEMISC \_ SETCLIENTSITEFIRST-Bit wird möglicherweise nicht unbedingt von einem Container unterstützt. In diesen Fällen muss ein Steuerelement auf Standardwerte für die umgebungseigenschaften zurück greifen, die es erfordert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

 





