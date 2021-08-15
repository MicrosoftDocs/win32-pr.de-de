---
description: Die \_ NewEnum-Eigenschaft von Signers ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 866b85d8bfd5eee89a8c8766acb10baa024aa35e4f81b7d7289a6430d345fa6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898397"
---
# <a name="signers_newenum-property"></a>Signierer. \_ NewEnum-Eigenschaft

\[Die **\_ NewEnum-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten. Weitere Informationen finden Sie in der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **\_ NewEnum-Eigenschaft** ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.

## <a name="syntax"></a>Syntax


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt, das zum Aufzählen der Auflistung verwendet werden kann.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das `For Each In` -Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Unterzeichner**](signers.md)
</dt> </dl>

 

 
