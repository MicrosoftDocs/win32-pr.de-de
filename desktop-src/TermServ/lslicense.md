---
title: LSLicense-Struktur
description: Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- LSLicense-Struktur Remotedesktopdienste
- LPLSLicense-Strukturzeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ea276b1b1217505a7bb44e1d70dd58d53eb57933d755ed9f79100abc177c3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605413"
---
# <a name="lslicense-structure"></a>LSLicense-Struktur

Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.

> [!Note]  
> Diese Struktur ist in keiner Headerdatei definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Version der Lizenz.

</dd> <dt>

**dwLicenseId**
</dt> <dd>

ID der Lizenz.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID des [**LSKeyPack,**](lskeypack.md) das die Lizenz enthält.

</dd> <dt>

**szHWID**
</dt> <dd>

Hardware-ID des RDC-Clients (Remotedesktopverbindung), für den die Lizenz ausgestellt wurde.

</dd> <dt>

**szMachineName**
</dt> <dd>

Name des RDC-Clients (Remotedesktopverbindung), für den die Lizenz ausgestellt wurde.

</dd> <dt>

**szUserName**
</dt> <dd>

Name des Benutzers, der die Lizenz ausgestellt hat.

</dd> <dt>

**dwCertSerialLicense**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**dwLicenseSerialNumber**
</dt> <dd>

Seriennummer der Lizenz.

</dd> <dt>

**ftIssueDate**
</dt> <dd>

Datum, an dem die Lizenz ausgestellt wurde.

</dd> <dt>

**ftExpireDate**
</dt> <dd>

Datum, an dem die Lizenz abläuft.

</dd> <dt>

**ucLicenseStatus**
</dt> <dd>

Aktueller Status der Lizenz.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

 





