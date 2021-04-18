---
title: TS_LF_ Konstanten (textstor. h)
description: Die TS \_ LF \_ \-Konstanten geben den Typ der Dokument Sperre an.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341352"
---
# <a name="ts_lf_-constants"></a>TS \_ LF- \_ \* Konstanten

Die TS- \_ LF- \_ \* Konstanten geben den Typ der Dokument Sperre an.



| Konstante/Wert                                                                                                                                                                                                                    | BESCHREIBUNG                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <dt>**TS \_ LF \_ Synchronisieren**</dt> <dt>(0x1)</dt> </dl>                | Das Dokument hat eine synchrone Sperre, wenn dieses Flag mit anderen Flags kombiniert wird.<br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <dt>**TS \_ LF- \_ Lese**</dt> Vorgang <dt>(0x2)</dt> </dl>                | Das Dokument weist eine schreibgeschützte Sperre auf und kann nicht geändert werden.<br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <dt>**TS \_ LF- \_ Lesevorgang**</dt> <dt>(0x6)</dt> </dl> | Das Dokument hat eine Lese-/Schreibsperre und kann geändert werden.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Dokument Sperren](document-locks.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[Itextstoreanchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[Itextstoreanchorsink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





