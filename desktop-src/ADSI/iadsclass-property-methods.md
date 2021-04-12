---
title: Iadsclass-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsclass-Schnittstelle werden die folgenden Eigenschaften festgelegt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Iadsclass-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105153"
---
# <a name="iadsclass-property-methods"></a>Iadsclass-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle werden die folgenden Eigenschaften festgelegt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Kter**
</dt> <dd> <dl>

Boolescher Wert, der angibt, ob diese Klasse abstrakt oder nicht abstrakt ist. Wenn **true**, ist diese Klasse eine abstrakte Klasse und kann im Verzeichnisdienst nicht direkt instanziiert werden. Abstrakte Klassen können nur als Superklassen verwendet werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **boolescher** Wert
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**"Auxderivedfrom"**
</dt> <dd> <dl>

Array von ADsPath-Zeichen folgen, die die Super-Hilfssysteme angeben, von denen diese Klasse abgeleitet ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Sten**
</dt> <dd> <dl>

Boolescher Wert, der angibt, ob diese Klasse eine Hilfselemente ist. Wenn **true**, ist diese Klasse eine Hilfsklasse und kann nicht direkt im Verzeichnisdienst instanziiert werden. Erweiterungs Klassen können nur als Superklassen anderer Erweiterungs Klassen oder als Quelle zusätzlicher Eigenschaften für Struktur Klassen verwendet werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **boolescher** Wert
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**CLSID**
</dt> <dd> <dl>

Optionale anbieterspezifische CLSID, die das COM-Objekt identifiziert, das diese Klasse implementiert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Container**
</dt> <dd> <dl>

Boolescher Wert, der angibt, ob diese Klasse ein Container anderer Objektklassen sein kann. Wenn dieser Wert **true** ist, können Sie die **get \_ Container** -Methode zum Abrufen eines Arrays von Objektklassen abrufen, die diese Klasse enthalten kann.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **boolescher** Wert
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Containment**
</dt> <dd> <dl>

Ein **BSTR** -Array, in dem jedes Element der Name einer Objektklasse ist, die diese Klasse enthalten kann.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**Derivedfrom**
</dt> <dd> <dl>

Array von ADsPath-Zeichen folgen, die angeben, von welchen Klassen diese Klasse abgeleitet wurde.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Helpfilecontext**
</dt> <dd> <dl>

Die Kontext-ID in **helpfilename** , in der spezifische Informationen für diese Klasse gefunden werden können.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**Helpfilename**
</dt> <dd> <dl>

Der Name einer Hilfedatei, die weitere Informationen zu Objekten dieser Klasse enthält.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**MandatoryProperties**
</dt> <dd> <dl>

**SAFEARRAY** von **Variant** s, die die Eigenschaften auflistet, die festgelegt werden müssen, damit diese Klasse in den Speicher geschrieben wird. Wenn die Klasse nur eine Eigenschaft enthält, gibt **get \_ MandatoryProperties** einen **BSTR** zurück.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**Namingproperties**
</dt> <dd> <dl>

**SAFEARRAY** von **BSTR** s, das die Eigenschaften auflistet, die zum Benennen von Attributen dieser Schema Klasse verwendet werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**OID**
</dt> <dd> <dl>

Anbieter spezifischer Objekt Bezeichner, der diese Klasse definiert. Dies wird bereitgestellt, um die Schema Erweiterung mithilfe von Active Directory in Verzeichnisdiensten zuzulassen, die anbieterspezifische OIDs für Klassen erfordern.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**SAFEARRAY** von **Variant** s, die die optionalen Eigenschaften für diese Schema Klasse auflistet. Wenn die Klasse nur eine Eigenschaft enthält, gibt **get \_ OptionalProperties** einen **BSTR** zurück.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**Possiblevorgesetzten**
</dt> <dd> <dl>

Array von ADsPath-Zeichen folgen, die die Schema Klassen angeben, die Instanzen dieser Klasse enthalten können.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**Primaryinterface**
</dt> <dd> <dl>

Optionaler Anbieter spezifischer Bezeichner-GUID, der Objekten dieser Schema Klasse eine Schnittstelle zuordnet. Beispielsweise wird die "User"-Klasse, die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) und **primaryinterface** unterstützt, durch **IID \_ IADsUser** identifiziert. Dies muss das Standard Zeichen folgen Format einer GUID aufweisen, wie durch com definiert. Diese GUID ist der Wert, der in der [**IADs:: get- \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) -Eigenschaft in Instanzen dieser Klasse für Anbieter angezeigt wird, die diese Eigenschaft implementieren. Durch die Identifizierung einer Schema Klasse durch die IID der primären Schnittstelle des Klassen Codes kann die Verwendung von **QueryInterface** zur Laufzeit bestimmt werden, ob ein Objekt der gewünschten Klasse entspricht.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie die [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle verwendet wird, um zu bestimmen, ob ein Objekt ein Container sein kann. wenn dies der Fall ist, werden die Namen aller enthaltenen Objekte aufgelistet.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



Im folgenden Codebeispiel wird gezeigt, wie die [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle verwendet wird, um zu bestimmen, ob ein Objekt ein Container sein kann. wenn dies der Fall ist, werden die Namen aller enthaltenen Objekte aufgelistet.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsclass ist als C8F93DD0-4AE0-11CF-9E73-00AA004A5691 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**Iadsclass:: Qualifizierer**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





