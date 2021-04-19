---
description: Die folgenden Flags geben die Ebene der dynamischen Verbindungs Verbindung an, die während des Renderings verwendet werden soll.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Dynamische reverbindungsflags (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369646"
---
# <a name="dynamic-reconnection-flags"></a>Dynamische neuverbindungsflags

\[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

Die folgenden Flags geben die Ebene der dynamischen Verbindungs Verbindung an, die während des Renderings verwendet werden soll.



| Konstante/Wert                                                                                                                                                                                                                                            | BESCHREIBUNG                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**Connectf \_ Dynamic \_ None**</dt> <dt>0x00</dt> </dl>          | Keine dynamische erneute Verbindung. Laden Sie alles, bevor Sie das Projekt rendern.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**Connectf \_ Dynamische \_ Quellen**</dt> <dt>0x01</dt> </dl> | Laden Sie Quellen nur nach Bedarf.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**Connectf \_ Dynamische \_ Effekte**</dt> <dt>0x02</dt> </dl> | Reserviert. Darf nicht verwendet werden.<br/>                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Unenderengine:: setdynamikreconnectlevel"**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




