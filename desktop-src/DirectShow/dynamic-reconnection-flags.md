---
description: Die folgenden Flags geben die Ebene der dynamischen Erneutverbindung an, die während des Renderings verwendet werden soll.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Dynamische Verbindungsflags (Qedit.h)
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
ms.openlocfilehash: f7bd2ff28c0928c59c632df501e6545b50707cfd948dd57e4ff1bd1cf01d1721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966240"
---
# <a name="dynamic-reconnection-flags"></a>Dynamische Verbindungsflags

\[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

Die folgenden Flags geben die Ebene der dynamischen Erneutverbindung an, die während des Renderings verwendet werden soll.



| Konstante/Wert                                                                                                                                                                                                                                            | BESCHREIBUNG                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ NONE**</dt> <dt>0x00</dt> </dl>          | Keine dynamische Wiederherstellung der Verbindung. Laden Sie alles, bevor Sie das Projekt rendern.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ DYNAMISCHE \_ QUELLEN**</dt> <dt>0x01</dt> </dl> | Laden Sie Quellen nur nach Bedarf.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ EFFECTS**</dt> <dt>0x02</dt> </dl> | Reserviert. Darf nicht verwendet werden.<br/>                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




