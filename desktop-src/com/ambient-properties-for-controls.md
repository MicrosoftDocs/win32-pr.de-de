---
title: Ambient-Eigenschaften für Steuerelemente
description: Ambient-Eigenschaften für Steuerelemente
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388430"
---
# <a name="ambient-properties-for-controls"></a>Ambient-Eigenschaften für Steuerelemente

Wenn ein Steuerelement überhaupt Umgebungs Eigenschaften unterstützt, muss es mindestens die Werte der folgenden Ambient-Eigenschaften unter den in der folgenden Tabelle aufgeführten Bedingungen beachten, wobei die Standard-DispIds verwendet werden.



| Ambient-Eigenschaft            | DISPID          | Kommentare/Bedingungen zur Verwendung                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Wenn das Gebiets Schema für das Steuerelement signifikant ist, z. b. für die Textausgabe<br/>                                                                                                                                                                                                                  |
| UserMode <br/>        | -709<br/> | Wenn sich das Steuerelement im Benutzermodus (Entwurfs Modus) und im Lauf Modus anders verhält<br/>                                                                                                                                                                                                          |
| Uidead<br/>           | -710<br/> | Wenn das Steuerelement auf Benutzeroberflächen Ereignisse reagiert, sollte es diese Ambient-Eigenschaft berücksichtigen.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Wenn das Steuerelement die direkte Größe von sich selbst unterstützt<br/>                                                                                                                                                                                                                             |
| Durch das shoching<br/>     | -712<br/> | Wenn das Steuerelement direkte Aktivierung und UI-Aktivierung unterstützt<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Nur wenn das Steuerelement als OLEMISC \_ acunglikebutton gekennzeichnet ist (d. h., es wird Unterstützung für mnetmonics-Tastatur bereitgestellt, daher muss [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) und [**IOleControl:: onmnetmonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) implementiert werden).<br/> |



 

Wie bereits beschrieben, erfordert die Verwendung von Ambients [**sowohl IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) ( [**für OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) als minimal) als auch [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (für [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) und [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).

Das OLEMISC \_ setclientsitefirst-Bit darf nicht notwendigerweise von einem Container unterstützt werden. In diesen Fällen muss ein Steuerelement auf die Standardwerte für die erforderlichen Umgebungs Eigenschaften zurückgreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

 





