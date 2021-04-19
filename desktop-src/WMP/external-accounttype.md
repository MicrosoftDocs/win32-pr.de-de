---
title: Extern. AccountType
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die AccountType-Eigenschaft ruft den Kontotyp des aktuellen Benutzers ab.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Externe. AccountType-Windows-Media Player
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
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366770"
---
# <a name="externalaccounttype"></a>Extern. AccountType

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **AccountType** -Eigenschaft ruft den Kontotyp des aktuellen Benutzers ab.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die den Kontotyp darstellt. Zeichen folgen, die verschiedene Konto Typen darstellen, werden im Online Store definiert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ruft den Kontotyp durch Aufrufen der [iwmpcontentpartner:: getcontentpartnerinfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) -Methode ab, die vom Plug-in des Online Stores implementiert wird. Wenn der aktuelle Benutzer beim Online Shop angemeldet ist oder das Plug-in die Anmelde Informationen des Benutzers zwischengespeichert hat, kann die **getcontentpartnerinfo** -Methode den Kontotyp des Benutzers bestimmen und ihn an den Windows-Media Player zurückgeben. Der Kontotyp ist eine Zeichenfolge, die von Windows Media Player nicht interpretiert wird. Stattdessen übergibt Windows Media Player die Zeichenfolge aus dem Plug-in des Online Stores an das Skript auf der Discovery-Seite des Online Stores.

Wenn der aktuelle Benutzer nicht beim Online Store angemeldet ist und das Plug-in des Online Stores keine zwischengespeicherten Anmelde Informationen für den Benutzer besitzt, ruft diese Eigenschaft die Zeichenfolge ab, die die **getcontentpartnerinfo** -Methode in dieser Situation zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. userloggedin**](external-userloggedin.md)
</dt> </dl>

 

 





