---
title: WINBIO_IDENTITY Struktur (winbio \_ types. h)
description: Enthält einen identifizierenden Wert, der einer biometrischen Vorlage zugeordnet ist.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103995"
---
# <a name="winbio_identity-structure"></a>Winbio- \_ Identitäts Struktur

Die **winbio- \_ Identitäts** Struktur enthält einen identifizierenden Wert, der einer biometrischen Vorlage zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>Member

<dl> <dt>

**Type**
</dt> <dd>

Gibt das Format der Identitätsinformationen an, die in dieser Struktur enthalten sind. Mögliche Werte:



| Wert                                                                                                                                                                                         | Bedeutung                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**winbio- \_ ID- \_ Typ \_ null**</dt> </dl>             | Der Vorlage ist keine ID zugeordnet.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**winbio- \_ ID- \_ Typ Platzhalter \_**</dt> </dl> | Die Struktur entspricht allen Vorlagen Identitäten.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**winbio- \_ ID- \_ \_ GUID-Typ**</dt> </dl>             | Die Struktur enthält eine GUID, die der Vorlage zugeordnet ist.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**winbio- \_ ID- \_ Typ- \_ sid**</dt> </dl>                | Die Struktur enthält die der Vorlage zugeordnete Konto-SID.<br/> |



 

</dd> <dt>

**Wert**
</dt> <dd>

Eine Union, die einen der folgenden Werte enthalten kann:

<dl> <dt>

**NULL**
</dt> <dd>

Enthält 1, wenn der **Typmember** ein **winbio- \_ ID- \_ Typ \_ null** ist.

</dd> <dt>

**Platzhalter**
</dt> <dd>

Enthält 1, wenn der **Typmember** ein **winbio- \_ ID- \_ Typplatzhalter \_** ist.

</dd> <dt>

**Templateguid**
</dt> <dd>

Enthält einen 128-Bit-GUID-Wert, der die Vorlage identifiziert, wenn der **Typmember** eine **\_ \_ \_ GUID für den winbio-ID-Typ** ist.

</dd> <dt>

**AccountSid**
</dt> <dd>

Eine-Struktur, die eine Konto-sid enthält, wenn der **Typmember** den **winbio- \_ ID- \_ Typ \_ sid** hat.

<dl> <dt>

**Größe**
</dt> <dd>

Die Anzahl der Zeichen in der SID.

</dd> <dt>

**Daten**
</dt> <dd>

Ein Array von Zeichen ohne Vorzeichen, die die SID enthalten. Die aktuelle maximale Größe des Arrays beträgt 68 Zeichen.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in den folgenden Funktionen verwendet:

-   [**Winbiodeletetemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**Winbioregistricommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**Winbioenumregistrierungen**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**Winbiogetkredentialstate**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**Winbioidentifizierung**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**Winbioremovecredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**Winbioverify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**Winbioverifywithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> </dl>

 

 





