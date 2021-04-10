---
title: TS_IAS_ Konstanten (textstor. h)
description: Die TS \_ IAS \_ \-Konstanten werden als bitfeldflags verwendet, um das Einfügen von Text oder eingebetteten Objekten an einer Auswahl-oder Einfügemarke zu steuern.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103815"
---
# <a name="ts_ias_-constants"></a>TS \_ IAS- \_ \* Konstanten

Die TS \_ IAS- \_ \* Konstanten werden als bitfeldflags verwendet, um das Einfügen von Text oder eingebetteten Objekten an einer Auswahl-oder Einfügemarke zu steuern.



| Konstante/Wert                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**TS \_ IAS \_ noquery**</dt> <dt>(0x1)</dt> </dl>       | Der Text wird eingefügt, und der Bereichs Zeiger wird beim Beenden auf **null** festgelegt. Kann nicht mit dem TS \_ IAS- \_ Flag queryonly kombiniert werden.<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**TS \_ IAS- \_ queryonly**</dt> <dt>(0x2)</dt> </dl> | Führen Sie die Einfügung nicht aus. Für den Aufrufer muss nur der Bereichs Zeiger festgelegt werden. Kann nicht mit dem TS \_ IAS \_ noquery-Flag kombiniert werden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





