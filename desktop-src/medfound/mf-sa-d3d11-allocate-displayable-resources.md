---
description: Gibt an, ob der MFT-Beispiel Allocator (SA) die zugrunde liegende Direct3D-Textur mithilfe des D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE-Flags zuordnen soll.
title: MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES (MF Transform. h)
ms.topic: reference
ms.date: 03/31/2018
ms.openlocfilehash: ac70ee8c3015a2e08df2ee78b8051723707a1686
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107224025"
---
# <a name="mf_sa_d3d_allocate_displayable_resources-attribute"></a><span data-ttu-id="a46ec-103">MF \_ sa D3D Attribut "anzeigbare \_ \_ \_ \_ Ressourcen zuordnen"</span><span class="sxs-lookup"><span data-stu-id="a46ec-103">MF\_SA\_D3D\_ALLOCATE\_DISPLAYABLE\_RESOURCES attribute</span></span>

<span data-ttu-id="a46ec-104">Gibt an, ob der MFT-Beispiel Allocator (SA) die zugrunde liegende Direct3D-Textur mithilfe des [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) -Flags zuordnen soll.</span><span class="sxs-lookup"><span data-stu-id="a46ec-104">Specifies if the MFT’s Sample Allocator (SA) should allocate the underlying Direct3D Texture using the [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> 

## <a name="data-type"></a><span data-ttu-id="a46ec-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a46ec-105">Data type</span></span>

<span data-ttu-id="a46ec-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a46ec-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a46ec-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a46ec-107">Remarks</span></span>

<span data-ttu-id="a46ec-108">Dieses Attribut ist in Windows 10 Preview Build 14383 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a46ec-108">This attribute is available staring with Windows 10 Preview build 14383.</span></span> 

> [!NOTE]
> <span data-ttu-id="a46ec-109">Das **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** Member-Feld der [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) -Enumeration wird in einer zukünftigen Version des SDK verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a46ec-109">The **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** member field of the [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration will be available in a future release of the SDK.</span></span>

<span data-ttu-id="a46ec-110">Das **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** -Attribut wird vom Media Foundation Platt Form Ebene beim Rendern von Videos festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a46ec-110">The Media Foundation platform layer sets the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute when rendering video.</span></span> <span data-ttu-id="a46ec-111">Eine APP kann auch das Festlegen dieses Attributs aktivieren, wenn es einen eigenen Videorenderer implementieren und D3D11 anzeigbare Ressourcen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a46ec-111">An app could also opt to set this attribute if it wants to implement its own video renderer and make use of D3D11 Displayable Resources.</span></span> 

## <a name="example"></a><span data-ttu-id="a46ec-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a46ec-112">Example</span></span>

<span data-ttu-id="a46ec-113">Im folgenden Codebeispiel wird die Verwendung des **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** -Attributs veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a46ec-113">The following code example demonstrates the usage of the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="a46ec-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a46ec-114">Requirements</span></span>



| <span data-ttu-id="a46ec-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a46ec-115">Requirement</span></span> | <span data-ttu-id="a46ec-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a46ec-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a46ec-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a46ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a46ec-118">Windows 10 Preview-Build 14383</span><span class="sxs-lookup"><span data-stu-id="a46ec-118">Windows 10 Preview Build 14383</span></span><br/>                                    |
| <span data-ttu-id="a46ec-119">Header</span><span class="sxs-lookup"><span data-stu-id="a46ec-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a46ec-120"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a46ec-120"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a46ec-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a46ec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46ec-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a46ec-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a46ec-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a46ec-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a46ec-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a46ec-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a46ec-125">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a46ec-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




