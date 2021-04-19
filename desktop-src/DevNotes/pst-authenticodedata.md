---
description: Definiert die Daten, die in der Microsoft Authenticode-Überprüfung von Elementdaten verwendet werden sollen.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370088"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="b4a3c-103">PST- \_ authenticodedata-Struktur</span><span class="sxs-lookup"><span data-stu-id="b4a3c-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="b4a3c-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b4a3c-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b4a3c-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b4a3c-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="b4a3c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b4a3c-108">Definiert die Daten, die in der Microsoft Authenticode-Überprüfung von Elementdaten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a3c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4a3c-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="b4a3c-110">Member</span><span class="sxs-lookup"><span data-stu-id="b4a3c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4a3c-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="b4a3c-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4a3c-112">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4a3c-113">**dwmodifier**</span><span class="sxs-lookup"><span data-stu-id="b4a3c-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="b4a3c-114">Ein Wert, der den Modifizierer identifiziert, der von einer Kette von Aufrufern überprüft werden muss.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="b4a3c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b4a3c-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="b4a3c-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b4a3c-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="b4a3c-117"><dt>**PST \_ AC \_ Single \_ Caller**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b4a3c-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="b4a3c-118">Nur eine einzelne Ebene in der Aufrufkette an den pstore.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="b4a3c-119">Der Aufrufer übergibt die Überprüfungs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-119">The caller passes the verification check.</span></span> <span data-ttu-id="b4a3c-120">Das angegebene Bild ist der unmittelbare Aufrufer, und ist eine Anwendung (. exe).</span><span class="sxs-lookup"><span data-stu-id="b4a3c-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="b4a3c-121"><dt>**PST \_ Rufer der \_ obersten \_ Ebene \_ der AC**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b4a3c-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b4a3c-122">Der Aufrufer der obersten Ebene muss die Überprüfung bestehen, es können jedoch zwischengeschaltete DLLs vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="b4a3c-123">Das angegebene Bild ist nicht notwendigerweise der unmittelbare Aufrufer, und ist eine Anwendung (. exe).</span><span class="sxs-lookup"><span data-stu-id="b4a3c-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="b4a3c-124"><dt>**PST \_ AC \_ immediate \_**</dt> -Aufrufer <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b4a3c-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="b4a3c-125">Der unmittelbare Aufrufer muss die Überprüfung bestehen, muss jedoch nicht der Prozess der obersten Ebene sein.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="b4a3c-126">Das angegebene Bild ist der unmittelbare Aufrufer, und das Bild kann eine Anwendung (. exe) oder eine DLL sein.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b4a3c-127">**szrootca**</span><span class="sxs-lookup"><span data-stu-id="b4a3c-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="b4a3c-128">Ein Zeiger auf eine Zeichenfolge mit breit Zeichen, die die Stamm Zertifizierungsstelle (Certification Authority, ca) für das Zertifikat darstellt. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="b4a3c-129">**szissuer**</span><span class="sxs-lookup"><span data-stu-id="b4a3c-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="b4a3c-130">Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die die Zertifizierungsstelle darstellt, die das Zertifikat ausgestellt hat. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="b4a3c-131">**szpublisher**</span><span class="sxs-lookup"><span data-stu-id="b4a3c-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="b4a3c-132">Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Software Herausgeber darstellt. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="b4a3c-133">**szprogramname**</span><span class="sxs-lookup"><span data-stu-id="b4a3c-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="b4a3c-134">Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Programmnamen darstellt. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4a3c-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4a3c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4a3c-135">Requirements</span></span>



| <span data-ttu-id="b4a3c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4a3c-136">Requirement</span></span> | <span data-ttu-id="b4a3c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b4a3c-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a3c-138">Header</span><span class="sxs-lookup"><span data-stu-id="b4a3c-138">Header</span></span><br/> | <dl> <span data-ttu-id="b4a3c-139"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a3c-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
