---
description: Definiert standardmäßige, spezifische und generische Rechte. Diese Rechte werden in Zugriffs Steuerungs Einträgen (Access Control Entries, ACEs) verwendet und sind das primäre Mittel zum Angeben des angeforderten oder gewährten Zugriffs auf ein Objekt.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131449"
---
# <a name="access_mask"></a><span data-ttu-id="ad638-104">Zugriffs \_ Maske</span><span class="sxs-lookup"><span data-stu-id="ad638-104">ACCESS\_MASK</span></span>

<span data-ttu-id="ad638-105">Der **Access \_ Mask** -Datentyp ist ein **DWORD** -Wert, der Standard-, spezifische und generische Rechte definiert.</span><span class="sxs-lookup"><span data-stu-id="ad638-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="ad638-106">Diese Rechte werden in [*Zugriffs Steuerungs Einträgen (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs) verwendet und sind das primäre Mittel zum Angeben des angeforderten oder gewährten Zugriffs auf ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad638-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="ad638-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad638-107">Remarks</span></span>

<span data-ttu-id="ad638-108">Die Bits in diesem Wert werden wie folgt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ad638-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="ad638-109">Bits</span><span class="sxs-lookup"><span data-stu-id="ad638-109">Bits</span></span>             | <span data-ttu-id="ad638-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ad638-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad638-111">0 15</span><span class="sxs-lookup"><span data-stu-id="ad638-111">0 15</span></span><br/>  | <span data-ttu-id="ad638-112">Bestimmte Rechte.</span><span class="sxs-lookup"><span data-stu-id="ad638-112">Specific rights.</span></span> <span data-ttu-id="ad638-113">Enthält die für den Objekttyp spezifische Zugriffs Maske, die der Maske zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ad638-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ad638-114">16 23</span><span class="sxs-lookup"><span data-stu-id="ad638-114">16 23</span></span><br/> | <span data-ttu-id="ad638-115">Standard Rechte.</span><span class="sxs-lookup"><span data-stu-id="ad638-115">Standard rights.</span></span> <span data-ttu-id="ad638-116">Enthält die Standard Zugriffsrechte des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad638-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ad638-117">24</span><span class="sxs-lookup"><span data-stu-id="ad638-117">24</span></span><br/>    | <span data-ttu-id="ad638-118">Zugreifen auf die Systemsicherheit (**Zugriffs \_ System \_ Sicherheit**).</span><span class="sxs-lookup"><span data-stu-id="ad638-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="ad638-119">Es wird verwendet, um den Zugriff auf eine SACL ( [*System Access Control List*](/windows/desktop/SecGloss/s-gly) ) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad638-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="ad638-120">Diese Art von Zugriff erfordert, dass der Aufrufprozess über die Berechtigung **SE \_ Security \_ Name** (Überwachungs-und Sicherheitsprotokoll verwalten) verfügt.</span><span class="sxs-lookup"><span data-stu-id="ad638-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="ad638-121">Wenn dieses Flag in der Zugriffs Maske eines Überwachungs Zugriffs-ACE (erfolgreicher oder nicht erfolgreicher Zugriff) festgelegt ist, wird der Zugriff auf die SACL überwacht.</span><span class="sxs-lookup"><span data-stu-id="ad638-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="ad638-122">25</span><span class="sxs-lookup"><span data-stu-id="ad638-122">25</span></span><br/>    | <span data-ttu-id="ad638-123">Maximal zulässig (**maximal \_ zulässig**).</span><span class="sxs-lookup"><span data-stu-id="ad638-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ad638-124">26 27</span><span class="sxs-lookup"><span data-stu-id="ad638-124">26 27</span></span><br/> | <span data-ttu-id="ad638-125">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad638-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ad638-126">28</span><span class="sxs-lookup"><span data-stu-id="ad638-126">28</span></span><br/>    | <span data-ttu-id="ad638-127">Generisch,**alle \_ (generisch**).</span><span class="sxs-lookup"><span data-stu-id="ad638-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ad638-128">29</span><span class="sxs-lookup"><span data-stu-id="ad638-128">29</span></span><br/>    | <span data-ttu-id="ad638-129">Generisch ausführen (**generisches \_ Ausführen**).</span><span class="sxs-lookup"><span data-stu-id="ad638-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ad638-130">30</span><span class="sxs-lookup"><span data-stu-id="ad638-130">30</span></span><br/>    | <span data-ttu-id="ad638-131">Generischer Schreibvorgang (**generischer \_ Schreib** Vorgang).</span><span class="sxs-lookup"><span data-stu-id="ad638-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ad638-132">31</span><span class="sxs-lookup"><span data-stu-id="ad638-132">31</span></span><br/>    | <span data-ttu-id="ad638-133">Generischer Lesevorgang (**generischer \_ Lese** Vorgang).</span><span class="sxs-lookup"><span data-stu-id="ad638-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="ad638-134">Die Standardrechte Bits (16 bis 23) enthalten die Standard Zugriffsrechte des Objekts und können eine Kombination der folgenden vordefinierten Flags sein.</span><span class="sxs-lookup"><span data-stu-id="ad638-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="ad638-135">bit</span><span class="sxs-lookup"><span data-stu-id="ad638-135">Bit</span></span>           | <span data-ttu-id="ad638-136">Flag</span><span class="sxs-lookup"><span data-stu-id="ad638-136">Flag</span></span>                         | <span data-ttu-id="ad638-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ad638-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad638-138">16</span><span class="sxs-lookup"><span data-stu-id="ad638-138">16</span></span><br/> | <span data-ttu-id="ad638-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ad638-139">**DELETE**</span></span><br/>        | <span data-ttu-id="ad638-140">Löschen Sie den Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ad638-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="ad638-141">17</span><span class="sxs-lookup"><span data-stu-id="ad638-141">17</span></span><br/> | <span data-ttu-id="ad638-142">**Lese \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="ad638-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="ad638-143">Lesezugriff auf den Besitzer, die Gruppe und die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) der Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="ad638-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="ad638-144">18</span><span class="sxs-lookup"><span data-stu-id="ad638-144">18</span></span><br/> | <span data-ttu-id="ad638-145">**\_DAC schreiben**</span><span class="sxs-lookup"><span data-stu-id="ad638-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="ad638-146">Schreibzugriff auf die DACL.</span><span class="sxs-lookup"><span data-stu-id="ad638-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="ad638-147">19</span><span class="sxs-lookup"><span data-stu-id="ad638-147">19</span></span><br/> | <span data-ttu-id="ad638-148">**\_Besitzer schreiben**</span><span class="sxs-lookup"><span data-stu-id="ad638-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="ad638-149">Schreibzugriff auf Besitzer.</span><span class="sxs-lookup"><span data-stu-id="ad638-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="ad638-150">20</span><span class="sxs-lookup"><span data-stu-id="ad638-150">20</span></span><br/> | <span data-ttu-id="ad638-151">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="ad638-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="ad638-152">Synchronisieren Sie den Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ad638-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="ad638-153">Die folgenden Konstanten, die in Winnt. h definiert sind, stellen die spezifischen und standardmäßigen Zugriffsrechte dar.</span><span class="sxs-lookup"><span data-stu-id="ad638-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="ad638-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad638-154">Requirements</span></span>



| <span data-ttu-id="ad638-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad638-155">Requirement</span></span> | <span data-ttu-id="ad638-156">Wert</span><span class="sxs-lookup"><span data-stu-id="ad638-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad638-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad638-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ad638-158">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad638-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ad638-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad638-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ad638-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad638-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ad638-161">Header</span><span class="sxs-lookup"><span data-stu-id="ad638-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad638-162"><dt>WinNT. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad638-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad638-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad638-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad638-164">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="ad638-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="ad638-165">Grundlegende Access Control Strukturen</span><span class="sxs-lookup"><span data-stu-id="ad638-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="ad638-166">Zugriffsrechte und Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="ad638-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="ad638-167">**generische \_ Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="ad638-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

