---
description: Gibt das Schutzschema für verschlüsselte Beispiele an.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: MFSampleExtension_Encryption_ProtectionScheme-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131121"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>MF SampleExtension- \_ Verschlüsselungs \_ Schema-Attribut

Gibt das Schutzschema für verschlüsselte Beispiele an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**mfsampleverschlüsseltionschutzscheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) -Enumeration. In Fällen, in denen die Medienquelle MP4-basiert ist, wird der Wert basierend auf dem Wert des **Felds \_ Schematyp** innerhalb des Felds Schematyp ("schm") im MP4-Header ("muov" oder "muof") festgelegt.

Wenn das Feld " **\_ Schematyp** " in einer MP4-basierten Datei lautet, oder Stream, ist auf ' Cenc ' oder ' cbc1 ' festgelegt, dann sollte das **mfsampleextension- \_ Verschlüsselungsschutz \_ Schema** -Attribut auf das **Schutz \_ Schema \_ AES- \_ CTR** oder das **Schutz \_ Schema \_ CBC** festgelegt werden, und es sollten keine Werte für die [mfsampleextension- \_ Verschlüsselung \_ cryptbyteblock](mfsampleextension-encryption-cryptbyteblock.md) und die [mfsampleextension- \_ Verschlüsselung \_ skipbyte](mfsampleextension-encryption-skipbyteblock.md)

Wenn das Feld für den **\_ Schematyp** in einer MP4-basierten Datei oder einem Stream auf ' CENs ' oder ' CBCs ' festgelegt ist, anschließend sollte das **mfsampleextension- \_ Verschlüsselungsschutz \_ Schema** -Attribut auf das **Schutz \_ Schema \_ AES- \_ CTR** oder das **Schutz \_ Schema \_ CBC** festgelegt werden. Außerdem muss die [mfsampleextension- \_ Verschlüsselung " \_ cryptbyteblock](mfsampleextension-encryption-cryptbyteblock.md) " und " [mfsampleextension \_ Encryption \_ skipbyteblock](mfsampleextension-encryption-skipbyteblock.md) " mithilfe der Werte im Feld "tenc" festgelegt werden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das **\_ Verschlüsselungs \_ Schema für die mfsampleextension** -Verschlüsselung und die zugeordneten Attribute " **\_ \_ cryptbyteblock** " und " **mfsampleextension Encryption" für \_ \_ skipbyteblock** -Verschlüsselung festgelegt werden.


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



 

 
