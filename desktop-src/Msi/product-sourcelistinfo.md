---
description: Die SourceListInfo-Eigenschaft des Product-Objekts ruft die Quellinformationseigenschaften für ein Produkt ab und legt sie fest. Diese Eigenschaft ruft MsiSourceListGetInfo oder MsiSourceListSetInfo auf. Dies ist eine Lese- oder Schreibeigenschaft.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Product.SourceListInfo (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d58bc3f9eae1f953d67d2bd83b951bda1d2fe17f3f2b00cbaa9b5b7f9ad3a968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376703"
---
# <a name="productsourcelistinfo-property"></a>Product.SourceListInfo (Eigenschaft)

Die **SourceListInfo-Eigenschaft** des [**Product-Objekts**](product-object.md) ruft die Quellinformationseigenschaften für ein Produkt ab und legt sie fest. Diese Eigenschaft ruft [**MsiSourceListGetInfo oder**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) [**MsiSourceListSetInfo auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) Dies ist eine Lese- oder Schreibeigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Quellinformationseigenschaften für ein Produkt, das abfragt oder festgelegt werden soll. Mögliche Werte finden Sie im Abschnitt "Hinweise" dieses Themas.

## <a name="remarks"></a>Hinweise

Nicht alle Eigenschaften, die abgerufen werden können, können festgelegt werden. Der *szProperty-Parameter* kann einer der folgenden Werte sein.



| Eigenschaft         | Kann festgelegt werden? | Bedeutung                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | J        | Der Pfad relativ zum Stamm des Installationsmediums.                                                                                                                                                                                                       |
| DiskPrompt       | J        | Die Eingabeaufforderungsvorlage, die verwendet wird, wenn der Benutzer zur Eingabe von Installationsmedien aufgefordert wird.                                                                                                                                                                                       |
| LastUsedSource   | J        | Der zuletzt verwendete Quellspeicherort für das Produkt. Wenn Sie diese Eigenschaft festlegen, stellen Sie dem Quellspeicherort "n;" für eine Netzwerkquelle oder "u;" als URL-Typ voran. Beispiel: "n; \\ \\ Scratch \\ Scratch \\ MySource" und "u; https://MyServer/MyFolder/MySource ". |
| LastUsedType     | N        | "n", wenn die zuletzt verwendete Quelle ein Netzwerkspeicherort ist. "u", wenn die zuletzt verwendete Quelle ein URL-Speicherort war. "m", wenn die zuletzt verwendete Quelle Medien war. Leere Zeichenfolge (""), wenn es keine zuletzt verwendete Quelle gibt.                                                                   |
| PackageName      | J        | Der Name des Pakets Windows Installer oder des Patchpakets in der Quelle.                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




