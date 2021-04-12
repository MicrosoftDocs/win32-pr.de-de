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
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="7071e-103">MF SampleExtension- \_ Verschlüsselungs \_ Schema-Attribut</span><span class="sxs-lookup"><span data-stu-id="7071e-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="7071e-104">Gibt das Schutzschema für verschlüsselte Beispiele an.</span><span class="sxs-lookup"><span data-stu-id="7071e-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="7071e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7071e-105">Data type</span></span>

<span data-ttu-id="7071e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7071e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7071e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7071e-107">Remarks</span></span>

<span data-ttu-id="7071e-108">Der Wert dieses Attributs ist ein Member der [**mfsampleverschlüsseltionschutzscheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="7071e-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="7071e-109">In Fällen, in denen die Medienquelle MP4-basiert ist, wird der Wert basierend auf dem Wert des **Felds \_ Schematyp** innerhalb des Felds Schematyp ("schm") im MP4-Header ("muov" oder "muof") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7071e-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="7071e-110">Wenn das Feld " **\_ Schematyp** " in einer MP4-basierten Datei lautet, oder Stream, ist auf ' Cenc ' oder ' cbc1 ' festgelegt, dann sollte das **mfsampleextension- \_ Verschlüsselungsschutz \_ Schema** -Attribut auf das **Schutz \_ Schema \_ AES- \_ CTR** oder das **Schutz \_ Schema \_ CBC** festgelegt werden, und es sollten keine Werte für die [mfsampleextension- \_ Verschlüsselung \_ cryptbyteblock](mfsampleextension-encryption-cryptbyteblock.md) und die [mfsampleextension- \_ Verschlüsselung \_ skipbyte](mfsampleextension-encryption-skipbyteblock.md)</span><span class="sxs-lookup"><span data-stu-id="7071e-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="7071e-111">Wenn das Feld für den **\_ Schematyp** in einer MP4-basierten Datei oder einem Stream auf ' CENs ' oder ' CBCs ' festgelegt ist, anschließend sollte das **mfsampleextension- \_ Verschlüsselungsschutz \_ Schema** -Attribut auf das **Schutz \_ Schema \_ AES- \_ CTR** oder das **Schutz \_ Schema \_ CBC** festgelegt werden. Außerdem muss die [mfsampleextension- \_ Verschlüsselung " \_ cryptbyteblock](mfsampleextension-encryption-cryptbyteblock.md) " und " [mfsampleextension \_ Encryption \_ skipbyteblock](mfsampleextension-encryption-skipbyteblock.md) " mithilfe der Werte im Feld "tenc" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7071e-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="7071e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7071e-112">Examples</span></span>

<span data-ttu-id="7071e-113">Im folgenden Beispiel wird gezeigt, wie das **\_ Verschlüsselungs \_ Schema für die mfsampleextension** -Verschlüsselung und die zugeordneten Attribute " **\_ \_ cryptbyteblock** " und " **mfsampleextension Encryption" für \_ \_ skipbyteblock** -Verschlüsselung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7071e-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7071e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7071e-114">Requirements</span></span>



| <span data-ttu-id="7071e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7071e-115">Requirement</span></span> | <span data-ttu-id="7071e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7071e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7071e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7071e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7071e-118">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7071e-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7071e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7071e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7071e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7071e-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="7071e-121">Header</span><span class="sxs-lookup"><span data-stu-id="7071e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7071e-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7071e-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
