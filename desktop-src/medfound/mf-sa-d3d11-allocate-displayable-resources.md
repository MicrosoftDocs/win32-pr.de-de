---
description: Gibt an, ob die Sample Allocator (SA) des MFT die zugrunde liegende Direct3D-Textur mithilfe des D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE zuordnen soll.
title: MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES (Mftransform.h)
ms.topic: reference
ms.date: 03/31/2018
ms.openlocfilehash: fedcfbe98344dd9b424c1a8ce90e847e98f1af51
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548705"
---
# <a name="mf_sa_d3d_allocate_displayable_resources-attribute"></a><span data-ttu-id="79096-103">MF \_ SA \_ D3D \_ ALLOCATE \_ DISPLAYABLE \_ RESOURCES-Attribut</span><span class="sxs-lookup"><span data-stu-id="79096-103">MF\_SA\_D3D\_ALLOCATE\_DISPLAYABLE\_RESOURCES attribute</span></span>

<span data-ttu-id="79096-104">Gibt an, ob die Sample Allocator (SA) des MFT die zugrunde liegende Direct3D-Textur mithilfe des D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE [zuordnen](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) soll.</span><span class="sxs-lookup"><span data-stu-id="79096-104">Specifies if the MFT’s Sample Allocator (SA) should allocate the underlying Direct3D Texture using the [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> 

## <a name="data-type"></a><span data-ttu-id="79096-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="79096-105">Data type</span></span>

<span data-ttu-id="79096-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="79096-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="79096-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79096-107">Remarks</span></span>

<span data-ttu-id="79096-108">Dieses Attribut ist mit dem Windows 10 Build 20348 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79096-108">This attribute is available staring with Windows 10 build 20348.</span></span> 

> [!NOTE]
> <span data-ttu-id="79096-109">Das **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE-Memberfeld** der [](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) D3D11_RESOURCE_MISC_FLAG wird in einer zukünftigen Version des SDK verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="79096-109">The **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** member field of the [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration will be available in a future release of the SDK.</span></span>

<span data-ttu-id="79096-110">Die Media Foundation-Plattformebene legt **das** MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES beim Rendern von Videos fest.</span><span class="sxs-lookup"><span data-stu-id="79096-110">The Media Foundation platform layer sets the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute when rendering video.</span></span> <span data-ttu-id="79096-111">Eine App kann dieses Attribut auch festlegen, wenn sie einen eigenen Videorenderer implementieren und D3D11 Displayable Resources verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="79096-111">An app could also opt to set this attribute if it wants to implement its own video renderer and make use of D3D11 Displayable Resources.</span></span> 

## <a name="example"></a><span data-ttu-id="79096-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="79096-112">Example</span></span>

<span data-ttu-id="79096-113">Im folgenden Codebeispiel wird die Verwendung des -Attributs MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES **veranschaulicht.**</span><span class="sxs-lookup"><span data-stu-id="79096-113">The following code example demonstrates the usage of the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute.</span></span>

```cpp
class DecoderMFT : public IMFAttributes, public IMFTransform 
{ 
    //  
    ... Other implementation details ommitted 
    // 

public: 
    // Implementation of IMFAttributes::GetAttributes which is invoked by the MF Topology Loader 
    STDMETHODIMP GetAttribtues(IMFAttributes** attributes) 
    { 
        m_attributes.copyTo(attributes); 
        return S_OK; 
    } 

 

private: 
    // Private method to be called before DecoderMFT initializes its sample pool. 
    // A good place for this to happen is in the method which processes the  
    // 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING' event. 
    // At a minimum, this processing would be in DecoderMFT's implementation of IMFTransform::ProcessMessage.  

    HRESULT ConfigureTextureFlags() 
    { 
        UINT32 allocateDisplayables = MFGetAttributeUINT32(m_attributes.get(), 
            MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES, 0); 

        // If no MF_SA_* attributes which correspond to D3D misc flags are set then it is valid for 
        // miscFlags to be set to 0. 
        m_textureDesc.miscFlags = 0; 
        UINT32 sharedResources = 0; 

        if (allocateDisplayables != 0) 
        { 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_DISPLAYABLE; 
            // The following flag is required for the decoders output to 
            // use D3D11_RESOURCE_MISC_DISPLAYABLE. 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_EXCLUSIVE_WRITER; 

            // The following flags are required for the presentation API 
            // to consume and present these resources (also known as direct presentation). 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED_NTHANDLE; 

            sharedResources = 1; 
        } 
        else  
        { 
            // This handles the case when MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES was 0 or missing. 
            sharedResources = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED_WITHOUT_MUTEX, 0); 

            if (sharedResources != 0) 
            { 
                m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            } 
            else 
            { 
                UINT32 sharedKeyMutex = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED, 0); 

                if (sharedKeyMutex != 0) 
                { 
                    m_textureDesc.micsFlags |= D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX; 
                } 
            } 
        } 

        // Processing for other MF_SA_* attributes which imply D3D11_RESOURCE_MISC flag 
        // omitted from this sample. 

        return S_OK; 

    } 

    // Private method showing how DecoderMFT can create a texture with the flags required 
    // to satisfy "MF_SA_D3D11_ALLOCATE_DISPLAYBLE_RESOURCES".  
    // Because this is a private function we know the passed in pointer is always valid. 
    // This would be invoked by another private DecoderMFT function when allocating an MFSample 
    // for its sample pool. 

    HRESULT AllocateTextureForSample(ID3D11Texture2D** texture2D) 
    { 
        return m_d3dDevice->CreateTexture2D(&m_textureDesc, nullptr, texture2D); 
    } 

    // ... other members omitted 
    wil::com_ptr_nothrow<IMFAttributes> m_attributes; 
    wil::com_ptr_nothrow<ID3D11Device> m_d3dDevice; 

    // This a texture description for D3D11 resources. 
    D3D11_TEXTURE_2D_DESC m_textureDesc = {}; 

}; 
```

## <a name="requirements"></a><span data-ttu-id="79096-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79096-114">Requirements</span></span>



| <span data-ttu-id="79096-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79096-115">Requirement</span></span> | <span data-ttu-id="79096-116">Wert</span><span class="sxs-lookup"><span data-stu-id="79096-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79096-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79096-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79096-118">Windows 10 Build 20348</span><span class="sxs-lookup"><span data-stu-id="79096-118">Windows 10 build 20348</span></span><br/>                                    |
| <span data-ttu-id="79096-119">Header</span><span class="sxs-lookup"><span data-stu-id="79096-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="79096-120"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="79096-120"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79096-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79096-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79096-122">Alphabetische Liste Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="79096-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79096-123">**ATTRIBUTEs::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="79096-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="79096-124">**ATTRIBUTEs::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="79096-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="79096-125">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="79096-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




