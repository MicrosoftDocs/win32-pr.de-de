---
title: IADsSecurityDescriptor-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsSecurityDescriptor-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften abgerufen oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- IADsSecurityDescriptor-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103498"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="6cc48-105">IADsSecurityDescriptor-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="6cc48-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="6cc48-106">Mit den Eigenschafts Methoden der [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6cc48-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="6cc48-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6cc48-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6cc48-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cc48-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6cc48-109">**Steuerung**</span><span class="sxs-lookup"><span data-stu-id="6cc48-109">**Control**</span></span>
<span data-ttu-id="6cc48-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-111">Flags, die die Bedeutung der Sicherheits Beschreibung qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="6cc48-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="6cc48-112">Werte werden aus der Win32- [**Sicherheits \_ \_ deskriptorsteuerungstruktur**](/windows/desktop/SecAuthZ/security-descriptor-control) entnommen.</span><span class="sxs-lookup"><span data-stu-id="6cc48-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="6cc48-113">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-114">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="6cc48-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-115">**Dacldefdefault**</span><span class="sxs-lookup"><span data-stu-id="6cc48-115">**DaclDefaulted**</span></span>
<span data-ttu-id="6cc48-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-117">Ein Flag des booleschen Typs, der angibt, ob die DACL von einem Standardmechanismus abgeleitet ist, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="6cc48-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="6cc48-118">Wenn der Ersteller eines Objekts z. b. keine DACL angibt, empfängt das Objekt die Standard-DACL vom Zugriffs Token des Erstellers.</span><span class="sxs-lookup"><span data-stu-id="6cc48-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="6cc48-119">Dieses Flag kann beeinflussen, wie das System die DACL behandelt, in Bezug auf die ACE-Vererbung.</span><span class="sxs-lookup"><span data-stu-id="6cc48-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="6cc48-120">Das System ignoriert dieses Flag, wenn das \_ Flag "SE DACL \_ Present" nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6cc48-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="6cc48-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-122">Skript Datentyp: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6cc48-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-123">**Diskretionaryacl**</span><span class="sxs-lookup"><span data-stu-id="6cc48-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="6cc48-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-125">Eine freigegebene Zugriffs Steuerungs Liste (DACL), die die Zugriffs Typen angibt, die dem-Objekt für angegebene Benutzer und Gruppen gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc48-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="6cc48-126">Weitere Informationen zu DACLs finden Sie unter [null-DACLs und leere DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="6cc48-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="6cc48-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-128">Skript Datentyp: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="6cc48-128">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-129">**Gruppieren**</span><span class="sxs-lookup"><span data-stu-id="6cc48-129">**Group**</span></span>
<span data-ttu-id="6cc48-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-131">Die Gruppe, zu der die Sicherheits-ID des Besitzers gehört.</span><span class="sxs-lookup"><span data-stu-id="6cc48-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="6cc48-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-133">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6cc48-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-134">**Gruppen Standard**</span><span class="sxs-lookup"><span data-stu-id="6cc48-134">**GroupDefaulted**</span></span>
<span data-ttu-id="6cc48-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-136">Ein Flag des booleschen Typs, der angibt, ob die Gruppendaten von einem Standardmechanismus abgeleitet werden, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="6cc48-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="6cc48-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-138">Skript Datentyp: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6cc48-138">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-139">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="6cc48-139">**Owner**</span></span>
<span data-ttu-id="6cc48-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-141">Objektbesitzer.</span><span class="sxs-lookup"><span data-stu-id="6cc48-141">Object owner.</span></span>

<dt>

<span data-ttu-id="6cc48-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-143">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6cc48-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-144">**Besitzer Standard**</span><span class="sxs-lookup"><span data-stu-id="6cc48-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="6cc48-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-146">Ein Flag des booleschen Typs, das angibt, dass die Besitzer Daten von einem Standardmechanismus abgeleitet werden, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="6cc48-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="6cc48-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-148">Skript Datentyp: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6cc48-148">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-149">**Novel**</span><span class="sxs-lookup"><span data-stu-id="6cc48-149">**Revision**</span></span>
<span data-ttu-id="6cc48-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-151">Revisions Ebene der Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="6cc48-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="6cc48-152">Dieser Wert wird aus der Win32- [**ACL- \_ Revisions \_ Informations**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) Struktur entnommen.</span><span class="sxs-lookup"><span data-stu-id="6cc48-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="6cc48-153">Alle ACEs in einer ACL müssen die gleiche Revisions Ebene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6cc48-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="6cc48-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-155">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="6cc48-155">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-156">**Sacldefault**</span><span class="sxs-lookup"><span data-stu-id="6cc48-156">**SaclDefaulted**</span></span>
<span data-ttu-id="6cc48-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-158">Ein Flag des booleschen Typs, das angibt, dass die SACL von einem Standardmechanismus abgeleitet ist, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="6cc48-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="6cc48-159">Dieses Flag kann Einfluss darauf haben, wie das System die SACL verarbeitet, in Bezug auf die ACE-Vererbung.</span><span class="sxs-lookup"><span data-stu-id="6cc48-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="6cc48-160">Das System ignoriert dieses Flag, wenn das \_ Flag für die SE SACL \_ Present nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6cc48-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="6cc48-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-162">Skript Datentyp: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6cc48-162">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6cc48-163">**SystemAcl**</span><span class="sxs-lookup"><span data-stu-id="6cc48-163">**SystemAcl**</span></span>
<span data-ttu-id="6cc48-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6cc48-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="6cc48-165">System Zugriffs Steuerungs Liste, die verwendet wird, um Überwachungsdaten Sätze für das-Objekt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6cc48-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="6cc48-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6cc48-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6cc48-167">Skript Datentyp: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="6cc48-167">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="6cc48-168">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cc48-168">Examples</span></span>

<span data-ttu-id="6cc48-169">Im folgenden Codebeispiel wird gezeigt, wie Sie eine vorhandene Sicherheits Beschreibung auflisten.</span><span class="sxs-lookup"><span data-stu-id="6cc48-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a><span data-ttu-id="6cc48-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cc48-170">Requirements</span></span>



| <span data-ttu-id="6cc48-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cc48-171">Requirement</span></span> | <span data-ttu-id="6cc48-172">Wert</span><span class="sxs-lookup"><span data-stu-id="6cc48-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc48-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cc48-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc48-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cc48-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="6cc48-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cc48-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc48-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cc48-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6cc48-177">Header</span><span class="sxs-lookup"><span data-stu-id="6cc48-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc48-178"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc48-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="6cc48-179">DLL</span><span class="sxs-lookup"><span data-stu-id="6cc48-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cc48-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cc48-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="6cc48-181">IID</span><span class="sxs-lookup"><span data-stu-id="6cc48-181">IID</span></span><br/>                      | <span data-ttu-id="6cc48-182">IID \_ IADsSecurityDescriptor ist als B8C787CA-9BDD-11D0-852C-00C04FD8D503 definiert.</span><span class="sxs-lookup"><span data-stu-id="6cc48-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6cc48-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc48-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc48-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6cc48-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="6cc48-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="6cc48-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="6cc48-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="6cc48-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

