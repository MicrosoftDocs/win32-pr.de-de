---
description: Diese Datentypen können verwendet werden, um den Typ eines Registrierungs Werts anzugeben.
title: Registrierungs Datentypen (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996594"
---
# <a name="registry-data-types"></a><span data-ttu-id="4503d-103">Registrierungs Datentypen</span><span class="sxs-lookup"><span data-stu-id="4503d-103">Registry Data Types</span></span>

<span data-ttu-id="4503d-104">Diese Datentypen können verwendet werden, um den Typ eines Registrierungs Werts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4503d-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="4503d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="4503d-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="4503d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4503d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="4503d-107"><dt>**REG- \_ Binärdatei**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="4503d-108">Binärdaten in beliebiger Form.</span><span class="sxs-lookup"><span data-stu-id="4503d-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="4503d-109"><dt>**REG \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="4503d-110">32-Bit-Nummer.</span><span class="sxs-lookup"><span data-stu-id="4503d-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="4503d-111"><dt>**REG \_ QWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="4503d-112">64-Bit-Nummer.</span><span class="sxs-lookup"><span data-stu-id="4503d-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="4503d-113"><dt>**REG \_ DWORD \_ Little- \_ umdian**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="4503d-114">32-Bit-Zahl im Little-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="4503d-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="4503d-115">Dies entspricht " **reg \_ DWORD**".</span><span class="sxs-lookup"><span data-stu-id="4503d-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="4503d-116">Im Little-Endian-Format wird ein multibytewert im Arbeitsspeicher vom niedrigsten Byte (dem "kleinen Ende") bis zum höchsten Byte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4503d-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="4503d-117">Beispielsweise wird der Wert 0x12345678 als (0x78 0x56 0x34 0x12) im Little-Endian-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4503d-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="4503d-118"><dt>**REG \_ QWORD \_ Little- \_ umdian**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="4503d-119">Eine 64-Bit-Zahl im Little-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="4503d-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="4503d-120">Dies entspricht " **reg \_ QWORD**".</span><span class="sxs-lookup"><span data-stu-id="4503d-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="4503d-121"><dt>**REG \_ DWORD Big-DWORD \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="4503d-122">32-Bit-Zahl im Big-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="4503d-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="4503d-123">Im Big-Endian-Format wird ein multibytewert im Arbeitsspeicher vom höchsten Byte (dem "großen Ende") bis zum niedrigsten Byte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4503d-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="4503d-124">Beispielsweise wird der Wert 0x12345678 als (0x12 0x34 0x56 0x78) im Big-Endian-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4503d-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="4503d-125"><dt>**REG \_ Expand \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="4503d-126">NULL-terminierte Zeichenfolge, die nicht erweiterte Verweise auf Umgebungsvariablen enthält (z. b. "% Path%").</span><span class="sxs-lookup"><span data-stu-id="4503d-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="4503d-127">Dabei handelt es sich um eine Unicode-oder ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode-oder ANSI-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4503d-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="4503d-128"><dt>**REG- \_ Link**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="4503d-129">Symbolische Unicode-Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="4503d-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="4503d-130"><dt>**REG \_ \_ MultiSZ**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="4503d-131">Array von auf NULL endenden Zeichen folgen, die mit zwei NULL-Zeichen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="4503d-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="4503d-132"><dt>**REG \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="4503d-133">Kein definierter Werttyp.</span><span class="sxs-lookup"><span data-stu-id="4503d-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="4503d-134"><dt>**REG- \_ Ressourcen \_ Liste**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="4503d-135">Gerätetreiber-Ressourcen Liste.</span><span class="sxs-lookup"><span data-stu-id="4503d-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="4503d-136"><dt>**REG- \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="4503d-137">Mit NULL endende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4503d-137">Null-terminated string.</span></span> <span data-ttu-id="4503d-138">Dabei handelt es sich um eine Unicode-oder ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode-oder ANSI-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4503d-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="4503d-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4503d-139">Requirements</span></span>



| <span data-ttu-id="4503d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4503d-140">Requirement</span></span> | <span data-ttu-id="4503d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="4503d-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4503d-142">Header</span><span class="sxs-lookup"><span data-stu-id="4503d-142">Header</span></span><br/> | <dl> <span data-ttu-id="4503d-143"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4503d-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




