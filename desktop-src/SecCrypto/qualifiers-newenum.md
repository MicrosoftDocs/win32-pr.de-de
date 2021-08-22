---
description: Die NewEnum-Eigenschaft von Qualifizierer ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Aufzählen der \_ Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
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
ms.openlocfilehash: b4d526b959720201769cb9d0bdf1fb65d679c225f91c7ed85c6aa4cbccca6bcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900976"
---
# <a name="qualifiers_newenum-property"></a>Qualifizierer. \_ NewEnum-Eigenschaft

\[Die **\_ NewEnum-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatrichtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinieninformationen in der Zertifikatrichtlinienerweiterung sind.\]

Die **\_ NewEnum-Eigenschaft** ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.

## <a name="syntax"></a>Syntax


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt, das zum Aufzählen der Auflistung verwendet werden kann.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das -Konstrukt `For Each In` in Visual Basic Scripting Edition (VBScript) verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Qualifikation**](qualifiers.md)
</dt> </dl>

 

 
