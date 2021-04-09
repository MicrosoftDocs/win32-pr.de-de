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
# <a name="iadssecuritydescriptor-property-methods"></a>IADsSecurityDescriptor-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften abgerufen oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Steuerung**
</dt> <dd> <dl>

Flags, die die Bedeutung der Sicherheits Beschreibung qualifizieren. Werte werden aus der Win32- [**Sicherheits \_ \_ deskriptorsteuerungstruktur**](/windows/desktop/SecAuthZ/security-descriptor-control) entnommen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Dacldefdefault**
</dt> <dd> <dl>

Ein Flag des booleschen Typs, der angibt, ob die DACL von einem Standardmechanismus abgeleitet ist, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden. Wenn der Ersteller eines Objekts z. b. keine DACL angibt, empfängt das Objekt die Standard-DACL vom Zugriffs Token des Erstellers. Dieses Flag kann beeinflussen, wie das System die DACL behandelt, in Bezug auf die ACE-Vererbung. Das System ignoriert dieses Flag, wenn das \_ Flag "SE DACL \_ Present" nicht festgelegt ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant \_ bool**
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

**Diskretionaryacl**
</dt> <dd> <dl>

Eine freigegebene Zugriffs Steuerungs Liste (DACL), die die Zugriffs Typen angibt, die dem-Objekt für angegebene Benutzer und Gruppen gewährt werden. Weitere Informationen zu DACLs finden Sie unter [null-DACLs und leere DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **IDispatch**
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

**Gruppieren**
</dt> <dd> <dl>

Die Gruppe, zu der die Sicherheits-ID des Besitzers gehört.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

**Gruppen Standard**
</dt> <dd> <dl>

Ein Flag des booleschen Typs, der angibt, ob die Gruppendaten von einem Standardmechanismus abgeleitet werden, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant \_ bool**
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

**Besitzer**
</dt> <dd> <dl>

Objektbesitzer.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

**Besitzer Standard**
</dt> <dd> <dl>

Ein Flag des booleschen Typs, das angibt, dass die Besitzer Daten von einem Standardmechanismus abgeleitet werden, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant \_ bool**
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

**Novel**
</dt> <dd> <dl>

Revisions Ebene der Sicherheits Beschreibung. Dieser Wert wird aus der Win32- [**ACL- \_ Revisions \_ Informations**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) Struktur entnommen. Alle ACEs in einer ACL müssen die gleiche Revisions Ebene aufweisen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Sacldefault**
</dt> <dd> <dl>

Ein Flag des booleschen Typs, das angibt, dass die SACL von einem Standardmechanismus abgeleitet ist, anstatt explizit vom ursprünglichen Anbieter der Sicherheits Beschreibung bereitgestellt zu werden. Dieses Flag kann Einfluss darauf haben, wie das System die SACL verarbeitet, in Bezug auf die ACE-Vererbung. Das System ignoriert dieses Flag, wenn das \_ Flag für die SE SACL \_ Present nicht festgelegt ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant \_ bool**
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

**SystemAcl**
</dt> <dd> <dl>

System Zugriffs Steuerungs Liste, die verwendet wird, um Überwachungsdaten Sätze für das-Objekt zu generieren.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **IDispatch**
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

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie Sie eine vorhandene Sicherheits Beschreibung auflisten.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsSecurityDescriptor ist als B8C787CA-9BDD-11D0-852C-00C04FD8D503 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

