---
description: Die \_ NewEnum-Eigenschaft von EKUs ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: c7d038c0-416f-47f7-94ba-74ca877da7ba
title: EKUs._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e34a625de7a9d27193629edca399121228cf09eef4f559aca04c7102e7bd4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767103"
---
# <a name="ekus_newenum-property"></a>EKUs. \_ NewEnum-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **\_ NewEnum-Eigenschaft** ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.

## <a name="syntax"></a>Syntax


```VB
EKUs._NewEnum As IUnknown
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt, das zum Aufzählen der Auflistung verwendet werden kann.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das `For Each In` -Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EKUs**](ekus.md)
</dt> </dl>

 

 
