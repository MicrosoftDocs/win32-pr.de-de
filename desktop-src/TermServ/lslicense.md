---
title: Lslicense-Struktur
description: Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Lslicense-Struktur Remotedesktopdienste
- Lplslicense-Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476440"
---
# <a name="lslicense-structure"></a>Lslicense-Struktur

Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**dwlicenseid**
</dt> <dd>

Die ID der Lizenz.

</dd> <dt>

**dwkeypackid**
</dt> <dd>

ID des [**lschräypack-Pakets**](lskeypack.md) , das die Lizenz enthält.

</dd> <dt>

**szhwid**
</dt> <dd>

Die Hardware-ID des Remotedesktopverbindung (RDC)-Clients, für den die Lizenz ausgestellt wurde.

</dd> <dt>

**szmachinename**
</dt> <dd>

Der Name des Remotedesktopverbindung (RDC)-Clients, für den die Lizenz ausgestellt wurde.

</dd> <dt>

**szusername**
</dt> <dd>

Der Name des Benutzers, der die Lizenz ausgestellt hat.

</dd> <dt>

**dwcertseriallicense**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**dwlicenseserialnumber**
</dt> <dd>

Seriennummer der Lizenz.

</dd> <dt>

**ftIssueDate**
</dt> <dd>

Datum, an dem die Lizenz ausgestellt wurde.

</dd> <dt>

**ftexpiredate**
</dt> <dd>

Datum, an dem die Lizenz abläuft.

</dd> <dt>

**uclicenstatusstatus**
</dt> <dd>

Aktueller Status der Lizenz.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lschräypack**](lskeypack.md)
</dt> <dt>

[**Tlslicenseenumbegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**Tlslicensitztenenumnext**](tlslicenseenumnext.md)
</dt> <dt>

[**Tlslicenabenumend**](tlslicenseenumend.md)
</dt> </dl>

 

 





