---
description: Die folgenden Konstanten werden von pstore verwendet.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Pstore-Konstanten (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361497"
---
# <a name="pstore-constants"></a><span data-ttu-id="41d9b-103">Pstore-Konstanten</span><span class="sxs-lookup"><span data-stu-id="41d9b-103">PStore Constants</span></span>

<span data-ttu-id="41d9b-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41d9b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="41d9b-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41d9b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="41d9b-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="41d9b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="41d9b-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="41d9b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="41d9b-108">Die folgenden Konstanten werden von pstore verwendet.</span><span class="sxs-lookup"><span data-stu-id="41d9b-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="41d9b-109">Fehler Codes bei geschützter Speicherung</span><span class="sxs-lookup"><span data-stu-id="41d9b-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="41d9b-110">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="41d9b-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="41d9b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41d9b-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="41d9b-112"><dt>**PST \_ E \_ OK**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="41d9b-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="41d9b-113">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="41d9b-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="41d9b-114"><dt>**PST \_ E- \_ Typ ist \_ vorhanden**</dt> <dt>0x800c0004l</dt></span><span class="sxs-lookup"><span data-stu-id="41d9b-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="41d9b-115">Das Datenelement ist bereits im geschützten Speicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41d9b-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="41d9b-116">Access-Klauselwerte</span><span class="sxs-lookup"><span data-stu-id="41d9b-116">Access Clause Values</span></span>



| <span data-ttu-id="41d9b-117">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="41d9b-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="41d9b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41d9b-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="41d9b-119"><dt>**PST \_ Authenticode**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="41d9b-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="41d9b-120">Verweist auf eine [**PST- \_ authenticodedata**](pst-authenticodedata.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="41d9b-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="41d9b-121"><dt> **PST- \_ Binär \_ Überprüfung**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="41d9b-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="41d9b-122">Verweist auf eine **PST \_ binarycheckdata** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="41d9b-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="41d9b-123"><dt>**PST \_ Sicherheits \_ Beschreibung**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="41d9b-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="41d9b-124">Verweist auf eine gültige Windows-Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="41d9b-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="41d9b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41d9b-125">Requirements</span></span>



| <span data-ttu-id="41d9b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41d9b-126">Requirement</span></span> | <span data-ttu-id="41d9b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="41d9b-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41d9b-128">Header</span><span class="sxs-lookup"><span data-stu-id="41d9b-128">Header</span></span><br/> | <dl> <span data-ttu-id="41d9b-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d9b-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
