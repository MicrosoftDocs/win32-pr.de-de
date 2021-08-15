---
description: Die FeatureState-Eigenschaft ist der Installationsstatus des Features für die Instanz dieses Produkts. Diese Eigenschaft ruft MsiQueryFeatureStateEx mit productCode, UserSid und Context des Objekts auf. Die Feature-ID wird als Parameter bereitgestellt.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Product.FeatureState-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 484b8f7f3094cf5bca2cb9d03941d68619995ba98de08e2845c3717439709e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129050"
---
# <a name="productfeaturestate-method"></a>Product.FeatureState-Methode

Die **FeatureState-Eigenschaft** ist der Installationsstatus des Features für die Instanz dieses Produkts.

Diese Eigenschaft ruft [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)mit *productCode,* *UserSid* und *Context* des Objekts auf. Die Feature-ID wird als Parameter bereitgestellt.

## <a name="syntax"></a>Syntax


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FeatureId* 
</dt> <dd>

Feature-ID, die in der Spalte Feature der [Featuretabelle](feature-table.md)angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Aufruf erfolgreich ist, enthält die -Eigenschaft den Wert als **DWORD.**



| State                    | Bedeutung                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ ANGEKÜNDIGT | Dieses Feature wird angekündigt.                  |
| INSTALLSTATE \_ LOCAL      | Das Feature wird lokal installiert.            |
| \_INSTALLSTATE-QUELLE     | Das Feature wird installiert, um von der Quelle aus ausgeführt zu werden. |



 

Wenn der Aufruf fehlschlägt, enthält die -Eigenschaft einen Fehlercode aus [**MsiQueryFeatureStateEx.**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)



| Fehler                     | Bedeutung                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLERZUGRIFF \_ \_ VERWEIGERT     | Der aufrufende Prozess muss über Administratorrechte verfügen, um Informationen zu einem Produkt abzurufen, das für einen anderen Benutzer als den aktuellen Benutzer installiert ist. |
| FEHLER: \_ FEHLERHAFTE \_ KONFIGURATION | Die Konfigurationsdaten sind beschädigt.                                                                                                         |
| FEHLER: \_ UNGÜLTIGER \_ PARAMETER | Ein ungültiger Parameter wurde an die Funktion übergeben.                                                                                           |
| FEHLER \_ ERFOLGREICH            | Die Funktion wurde erfolgreich abgeschlossen.                                                                                                       |
| \_ \_ FEHLER: UNBEKANNTES FEATURE   | Die Feature-ID identifiziert kein bekanntes Feature.                                                                                          |
| FEHLER \_ \_ UNBEKANNTES PRODUKT   | Der Produktcode identifiziert kein bekanntes Produkt.                                                                                        |
| \_ \_ FEHLERFUNKTION FEHLGESCHLAGEN   | Ein unerwarteter interner Fehler.                                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct ist als 000C10A0-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




