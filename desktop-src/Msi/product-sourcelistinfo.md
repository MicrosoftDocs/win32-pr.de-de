---
description: Die sourcelistinfo-Eigenschaft des Product-Objekts Ruft die Quell Informations Eigenschaften für ein Produkt ab und legt Sie fest. Diese Eigenschaft ruft msisourcelistgetinfo oder msisourcelist* tinfo auf. Dies ist eine Lese-oder Schreib Eigenschaft.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Product. sourcelistinfo-Eigenschaft
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
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371439"
---
# <a name="productsourcelistinfo-property"></a>Product. sourcelistinfo-Eigenschaft

Die **sourcelistinfo** -Eigenschaft des [**Product**](product-object.md) -Objekts Ruft die Quell Informations Eigenschaften für ein Produkt ab und legt Sie fest. Diese Eigenschaft ruft [**msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) oder [**msisourcelist* tinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)auf. Dies ist eine Lese-oder Schreib Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Quell Informations Eigenschaften für ein Produkt, das abgefragt oder festgelegt werden soll. Mögliche Werte finden Sie im Abschnitt "Hinweise" in diesem Thema.

## <a name="remarks"></a>Bemerkungen

Es können nicht alle Eigenschaften festgelegt werden, die abgerufen werden können. Der *szProperty* -Parameter kann einen der folgenden Werte aufweisen.



| Eigenschaft         | Kann festgelegt werden? | Bedeutung                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mediapackagepath | J        | Der Pfad relativ zum Stammverzeichnis des-Installationsmediums.                                                                                                                                                                                                       |
| Diskprompt       | J        | Die Eingabe Aufforderungs Vorlage, die verwendet wird, wenn der Benutzer zur Eingabe eines Installationsmediums                                                                                                                                                                                       |
| LastUsedSource   | J        | Der zuletzt verwendete Quell Speicherort für das Produkt. Wenn Sie diese Eigenschaft festlegen, legen Sie den Quell Speicherort für eine Netzwerkquelle oder "u;" für den URL-Typ als Präfix für den Quell Speicherort fest. Beispiel: "n; \\ \\ Scratch \\ Scratch \\ MySource "und" u; " https://MyServer/MyFolder/MySource . |
| Lastusedtype     | N        | "n", wenn die zuletzt verwendete Quelle ein Netzwerk Speicherort ist. "u", wenn die zuletzt verwendete Quelle ein URL-Speicherort war. "m", wenn die zuletzt verwendete Quelle Medien war. Leere Zeichenfolge (""), wenn keine zuletzt verwendete Quelle vorhanden ist.                                                                   |
| PackageName      | J        | Der Name des Windows Installer Pakets oder Patchpakets in der Quelle.                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Product**](product-object.md)
</dt> <dt>

[**Msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**Msisourcelisteintinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




