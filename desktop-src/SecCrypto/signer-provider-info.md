---
description: Gibt die Informationen des Kryptografiedienstanbieters (Cryptographic Service Provider, CSP) und des privaten Schlüssels an, die zum Erstellen einer digitalen Signatur verwendet werden.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO-Struktur
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
ms.openlocfilehash: 45ab23e4a568082de7e7fb4d23364ac6ba15c0f61378d54735cbc398e7e0e8ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898687"
---
# <a name="signer_provider_info-structure"></a>SIGNER \_ PROVIDER \_ INFO-Struktur

Die **SIGNER \_ PROVIDER \_ INFO-Struktur** gibt den [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (Cryptographic Service Provider, CSP) und informationen zum privaten Schlüssel an, die zum Erstellen einer digitalen Signatur verwendet werden.

> [!Note]  
> Diese Struktur ist in einer Headerdatei nicht definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**cbSize**
</dt> <dd>

Die Größe der -Struktur in Bytes.

</dd> <dt>

**pwszProviderName**
</dt> <dd>

Der Name des CSP, der zum Erstellen der digitalen Signatur verwendet wird. Wenn der Wert dieses Members **NULL ist,** wird der Standardanbieter verwendet.

</dd> <dt>

**dwProviderType**
</dt> <dd>

Der Vom **pwszProviderName-Member** angegebene CSP-Typ.

</dd> <dt>

**dwKeySpec**
</dt> <dd>

Die Schlüsselspezifikation. Wenn dieser Member auf 0 (null) festgelegt ist, wird die Schlüsselspezifikation im **pwszPvkFileName-** oder **pwszKeyContainer-Element** verwendet. Wenn im **pwszKeyContainer-Member** mehrere Schlüsselspezifikationen enthalten sind, wird **AT \_ SIGNATURE** verwendet. Wenn ein Fehler auftritt, **wird AT \_ KEYEXCHANGE** verwendet.

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Gibt den Typ der Informationen zum privaten Schlüssel an. Dieser Member kann mindestens einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                               | Bedeutung                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ GEBEN \_ SIE \_ DATEINAME**</dt> <dt>1 (0X1) EIN.</dt> </dl>         | Bei den Informationen des privaten Schlüssels handelt es sich um einen Dateinamen.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ TYPE \_ KEYCONTAINER**</dt> <dt>2 (0x2)</dt> </dl> | Die Informationen zum privaten Schlüssel sind ein Schlüsselcontainer.<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

Der Name der Datei, die die Informationen zum privaten Schlüssel enthält.

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

Der Name des Schlüsselcontainers, der die Informationen zum privaten Schlüssel enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
