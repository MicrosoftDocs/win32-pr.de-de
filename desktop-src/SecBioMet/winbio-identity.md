---
title: WINBIO_IDENTITY -Struktur (Winbio \_ types.h)
description: Enthält einen identifizierenden Wert, der einer biometrischen Vorlage zugeordnet ist.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY Struktur Windows Biometrieframework-API
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
ms.openlocfilehash: c677a341386bcc937061798f406397028c23c10b65989480da975a9fdf81a3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910118"
---
# <a name="winbio_identity-structure"></a>WINBIO \_ IDENTITY-Struktur

Die **WINBIO \_ IDENTITY-Struktur** enthält einen identifizierenden Wert, der einer biometrischen Vorlage zugeordnet ist.

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

**Typ**
</dt> <dd>

Gibt das Format der Identitätsinformationen an, die in dieser -Struktur enthalten sind. Mögliche Werte:



| Wert                                                                                                                                                                                         | Bedeutung                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_WINBIO-ID-TYP \_ \_ NULL**</dt> </dl>             | Der Vorlage ist keine ID zugeordnet.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ WINBIO-ID-TYP: \_ PLATZHALTER**</dt> </dl> | Die -Struktur stimmt mit allen Vorlagenidentitäten ab.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**GUID \_ DES WINBIO-ID-TYPS \_ \_**</dt> </dl>             | Die -Struktur enthält eine GUID, die der Vorlage zugeordnet ist.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**\_ \_ WINBIO-ID-TYP-SID \_**</dt> </dl>                | Die -Struktur enthält die Konto-SID, die der Vorlage zugeordnet ist.<br/> |



 

</dd> <dt>

**Wert**
</dt> <dd>

Eine Union, die einen der folgenden Werte enthalten kann:

<dl> <dt>

**NULL**
</dt> <dd>

Enthält 1, wenn **der Type-Member** **WINBIO \_ ID TYPE \_ NULL \_ ist.**

</dd> <dt>

**Platzhalter**
</dt> <dd>

Enthält 1, wenn **der Type-Member** **WINBIO \_ ID TYPE \_ \_ WILDCARD ist.**

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Enthält einen 128-Bit-GUID-Wert, der die Vorlage identifiziert, wenn der **Typ-Member** **WINBIO \_ ID TYPE \_ \_ GUID ist.**

</dd> <dt>

**AccountSid**
</dt> <dd>

Eine -Struktur, die eine Konto-SID enthält, wenn **das Type-Member** **WINBIO \_ ID TYPE \_ SID \_ ist.**

<dl> <dt>

**Größe**
</dt> <dd>

Die Anzahl der Zeichen in der SID.

</dd> <dt>

**Daten**
</dt> <dd>

Ein Array von Zeichen ohne Vorzeichen, die die SID enthalten. Die aktuelle maximale Größe des Arrays beträgt 68 Zeichen.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in den folgenden Funktionen verwendet:

-   [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> </dl>

 

 





