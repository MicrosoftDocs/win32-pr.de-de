---
description: Ruft die Auflistung der Benutzer Hinweis Nummern ab.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Qualifizierer. noticenumschlag (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370744"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="0a1fc-103">Qualifizierer. noticenumschlag (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0a1fc-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="0a1fc-104">\[Die **noticenumschlag** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0a1fc-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="0a1fc-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="0a1fc-106">Die **noticenumbers** -Eigenschaft ruft die Auflistung der Benutzer Hinweis Nummern ab.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="0a1fc-107">Diese Eigenschaft ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1fc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a1fc-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="0a1fc-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0a1fc-109">Property value</span></span>

<span data-ttu-id="0a1fc-110">Die Auflistung von Benutzer Hinweis Nummern.</span><span class="sxs-lookup"><span data-stu-id="0a1fc-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a1fc-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a1fc-111">Requirements</span></span>



| <span data-ttu-id="0a1fc-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a1fc-112">Requirement</span></span> | <span data-ttu-id="0a1fc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0a1fc-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1fc-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0a1fc-114">Redistributable</span></span><br/> | <span data-ttu-id="0a1fc-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a1fc-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0a1fc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0a1fc-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="0a1fc-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a1fc-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a1fc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a1fc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1fc-119">**Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="0a1fc-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
