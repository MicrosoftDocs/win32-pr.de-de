---
description: Die \_ Eigenschaft "netwenum" der Qualifizierer Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Qualifiers._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370648"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="d90b4-104">Qualifizierer. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="d90b4-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="d90b4-105">\[Die Eigenschaft " **\_ netwenum** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d90b4-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d90b4-106">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="d90b4-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="d90b4-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d90b4-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="d90b4-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d90b4-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="d90b4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90b4-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="d90b4-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d90b4-110">Property value</span></span>

<span data-ttu-id="d90b4-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d90b4-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="d90b4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d90b4-112">Remarks</span></span>

<span data-ttu-id="d90b4-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d90b4-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="d90b4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d90b4-114">Requirements</span></span>



| <span data-ttu-id="d90b4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d90b4-115">Requirement</span></span> | <span data-ttu-id="d90b4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d90b4-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d90b4-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d90b4-117">Redistributable</span></span><br/> | <span data-ttu-id="d90b4-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d90b4-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d90b4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d90b4-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="d90b4-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d90b4-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d90b4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d90b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90b4-122">**Qualifikation**</span><span class="sxs-lookup"><span data-stu-id="d90b4-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
