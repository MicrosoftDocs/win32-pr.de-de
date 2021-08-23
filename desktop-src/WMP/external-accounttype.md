---
title: External.accountType
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die accountType-Eigenschaft ruft den Kontotyp des aktuellen Benutzers ab.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External.accountType-Windows Media Player
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bd19413d891f5a8008b162f6795af29a9d15e75a80d35bb82ff13f8e013da9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650040"
---
# <a name="externalaccounttype"></a>External.accountType

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **accountType-Eigenschaft** ruft den Kontotyp des aktuellen Benutzers ab.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge,** die den Kontotyp darstellt. Zeichenfolgen, die verschiedene Kontotypen darstellen, werden vom Onlineshop definiert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ruft den Kontotyp ab, indem die [IWMPContentPartner::GetContentPartnerInfo-Methode](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) aufgerufen wird, die vom Plug-In des Onlineshops implementiert wird. Wenn der aktuelle Benutzer beim Onlineshop angemeldet ist oder das Plug-In die Anmeldeinformationen des Benutzers zwischengespeichert hat, kann die **getContentPartnerInfo-Methode** den Kontotyp des Benutzers bestimmen und an Windows Media Player. Der Kontotyp ist eine Zeichenfolge, die Windows Media Player nicht interpretiert. Stattdessen Windows Media Player die Zeichenfolge vom Plug-In des Onlineshops an das Skript auf der Ermittlungsseite des Onlineshops übergeben.

Wenn der aktuelle Benutzer nicht beim Onlineshop angemeldet ist und das Plug-In des Onlineshops nicht über zwischengespeicherte Anmeldeinformationen für den Benutzer verfügt, ruft diese Eigenschaft die Zeichenfolge ab, die die **getContentPartnerInfo-Methode** in dieser Situation zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





