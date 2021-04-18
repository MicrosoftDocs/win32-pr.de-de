---
description: Die folgenden GUIDs unterstützen CDM-Implementierungen (Content entschlüsseln Module).
title: CDM-GUIDs (Content Decryption Module)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364690"
---
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="d28f5-103">CDM-GUIDs (Content Decryption Module)</span><span class="sxs-lookup"><span data-stu-id="d28f5-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="d28f5-104">Die folgenden GUIDs unterstützen CDM-Implementierungen (Content entschlüsseln Module).</span><span class="sxs-lookup"><span data-stu-id="d28f5-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="d28f5-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="d28f5-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="d28f5-106">Dienst-GUID, die zum Abrufen von Schnittstellen aus einer [imfcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) -Implementierung verwendet wird, z. b. die WinRT-Schnittstelle [imediaschutzpmpserver](/uwp/api/windows.media.protection.mediaprotectionpmpserver)</span><span class="sxs-lookup"><span data-stu-id="d28f5-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="d28f5-107">Eine Implementierung von **IMF contentdecryptionmodule** sollte [IMF](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) implementieren und diese Dienst-GUID unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d28f5-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="d28f5-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d28f5-108">Requirements</span></span>



| <span data-ttu-id="d28f5-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d28f5-109">Requirement</span></span> | <span data-ttu-id="d28f5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d28f5-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d28f5-111">Header</span><span class="sxs-lookup"><span data-stu-id="d28f5-111">Header</span></span><br/> | <dl> <span data-ttu-id="d28f5-112"><dt>MF contentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="d28f5-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d28f5-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d28f5-113">See also</span></span>



- [<span data-ttu-id="d28f5-114">Media Foundation Konstanten</span><span class="sxs-lookup"><span data-stu-id="d28f5-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="d28f5-115">[IMF contentdecryptionmodule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="d28f5-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="d28f5-116">Imediaschutzpmpserver</span><span class="sxs-lookup"><span data-stu-id="d28f5-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="d28f5-117">IMF-Dienst</span><span class="sxs-lookup"><span data-stu-id="d28f5-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




