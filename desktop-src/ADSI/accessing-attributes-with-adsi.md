---
title: Zugreifen auf Attribute mit ADSI
description: Die IADs. Get-Methode und die IADs. Getex-Methode werden verwendet, um benannte Attributwerte abzurufen.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attribute, zugreifen mit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337252"
---
# <a name="accessing-attributes-with-adsi"></a>Zugreifen auf Attribute mit ADSI

Die [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode und die [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode werden verwendet, um benannte Attributwerte abzurufen. Beide Methoden geben einen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Wert zurück. Diese Methoden sind nur für Verzeichnisse verfügbar, die ein Schema unterstützen. Beim Zugriff auf Objekte in einem Verzeichnis ohne Schema müssen die Schnittstellen [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) und [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) verwendet werden, um Attributwerte zu bearbeiten.

Die Methoden [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) geben eine [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) zurück, die abhängig von der Anzahl der vom Server zurückgegebenen Werte ein **Variant** -Array sein kann oder nicht. Wenn z. b. nur ein Wert vom Server zurückgegeben wird, unabhängig davon, ob es sich um ein einzelnes oder mehr wertiges Attribut handelt, gibt die Methode eine einzelne **Variante** zurück. Umgekehrt wird ein **Variant** -Array zurückgegeben, wenn mehrere Werte zurückgegeben werden. Wenn ein **Variant** -Array zurückgegeben wird, enthält das **VT** -Element der **Variant** -Struktur die " **VT \_ Variant/vbVariant** "-und " **VT \_ Array/VBArray** "-Flags.

Die [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode und die [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode können mithilfe der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle auch ein COM-Objekt zurückgeben. In diesem Fall enthält das **VT** -Element der [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur das **VT \_ Dispatch/vbObject-** Flag. Um auf das COM-Objekt zuzugreifen, rufen Sie die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für die **IDispatch** -Schnittstelle auf, um die gewünschte Schnittstelle abzurufen.

Ein anderer Datentyp, der von [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -und [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methoden zurückgegeben wird, sind binäre Daten. In diesem Fall werden die Daten als zusammenhängendes Bytearray bereitgestellt, und der **VT** -Member der [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur enthält die **VT \_ UI1/vbByte** -und **VT \_ Array/VBArray** -Flags.

> [!Note]  
> Microsoft Visual Basic, die Skript Edition unterstützt nur [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -und **Variant** -Arrays. Daher kann VBScript nicht zum Lesen von binären Eigenschafts Werten verwendet werden.

 

Viele ADSI-Schnittstellen definieren Schnittstellen spezifische Eigenschaften. Die Schnittstelle [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) definiert z. b. die [**Location**](iadscomputer-property-methods.md) -Eigenschaft. Diese Schnittstellen definierten Eigenschaften können Daten enthalten, die mit einem der benannten Attribute identisch sind, aber die Eigenschaften sind spezifisch für den Objekttyp, auf den sich die Schnittstelle bezieht. In Sprachen, die Automation unterstützen, kann auf diese Schnittstellen definierten Eigenschaften mithilfe der Punkt Notation zugegriffen werden, wie im folgenden Codebeispiel gezeigt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie auf die ADsPath-Eigenschaft der IADs-Schnittstelle zugegriffen wird.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



In Sprachen, die nicht automatisiert werden, müssen die Eigenschaften Zugriffsmethoden für den Zugriff auf die Schnittstellen definierten Eigenschaften verwendet werden. Beispielsweise wird die [**iadscomputer:: get \_ Location**](iadscomputer-property-methods.md) -Methode zum Abrufen der **iadscomputer. Location** -Eigenschaft verwendet.

Im folgenden C++-Codebeispiel wird veranschaulicht, wie die-Eigenschaften Zugriffsmethode in C++ verwendet wird, um den ADsPath eines Benutzers abzurufen.


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



Weitere Informationen zum Zugreifen auf Attribute mit ADSI finden Sie unter:

-   [Die Get-Methode](the-get-method.md)
-   [Die Getex-Methode](the-getex-method.md)
-   [Die GetInfo-Methode](the-getinfo-method.md)
-   [Optimierung mithilfe von "GetInfoEx"](optimization-using-getinfoex.md)
-   [Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Beispiel Code zum Lesen von Attributen](example-code-for-reading-attributes.md)

 

 