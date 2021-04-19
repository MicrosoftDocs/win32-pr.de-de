---
description: Gibt die Informationen zum Kryptografiedienstanbieter (CSP) und zum privaten Schlüssel an, die zum Erstellen einer digitalen Signatur verwendet werden.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364134"
---
# <a name="signer_provider_info-structure"></a>\_Informationsstruktur des Signatur Geber Anbieters \_

Die Informationen Struktur des **Signatur \_ Geber Anbieters \_** gibt die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum privaten Schlüssel an, die zum Erstellen einer digitalen Signatur verwendet werden.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**pwszprovidername**
</dt> <dd>

Der Name des CSP, der zum Erstellen der digitalen Signatur verwendet wird. Wenn der Wert dieses Members **null** ist, wird der Standardanbieter verwendet.

</dd> <dt>

**dwprovidertype**
</dt> <dd>

Der vom **pwszprovidername** -Member angegebene Typ des CSP.

</dd> <dt>

**dwkeyspec**
</dt> <dd>

Die Schlüsselspezifikation. Wenn dieses Element auf 0 (null) festgelegt ist, wird die Schlüssel Spezifikation im Member **pwszpvkfilename** oder **pwszkeycontainer** verwendet. Wenn im **pwszkeycontainer** -Member mehr als eine Schlüssel Spezifikation vorhanden ist, wird **bei der \_ Signatur** verwendet. Wenn dies nicht möglich ist, wird **bei \_ keyexchange** verwendet.

</dd> <dt>

**dwpvkchoice**
</dt> <dd>

Gibt den Typ der Informationen zum privaten Schlüssel an. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                               | Bedeutung                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ \_ \_ Dateiname**</dt> <dt>1 (0x1)</dt> </dl>         | Die Informationen zum privaten Schlüssel sind ein Dateiname.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ Geben Sie \_ keycontainer**</dt> <dt>2 (0x2)</dt> ein. </dl> | Die Informationen zum privaten Schlüssel sind ein Schlüssel Container.<br/> |



 

</dd> <dt>

**pwszpvkfilename**
</dt> <dd>

Der Name der Datei, die die Informationen zum privaten Schlüssel enthält.

</dd> <dt>

**pwszkeycontainer**
</dt> <dd>

Der Name des Schlüssel Containers, der die Informationen zum privaten Schlüssel enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signersign**](signersign.md)
</dt> <dt>

[**Signersignetx**](signersignex.md)
</dt> </dl>

 

 
