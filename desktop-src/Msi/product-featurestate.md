---
description: Die Eigenschaft "featurestate" ist der Installationsstatus des Features für die Instanz dieses Produkts. Diese Eigenschaft ruft "msiqueryfeaturestateex" mit "ProductCode", "UserSID" und dem Kontext des-Objekts auf. Die Funktions-ID wird als Parameter bereitgestellt.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Product. featurestate-Methode
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
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366025"
---
# <a name="productfeaturestate-method"></a>Product. featurestate-Methode

Die Eigenschaft " **featurestate** " ist der Installationsstatus des Features für die Instanz dieses Produkts.

Diese Eigenschaft ruft " [**msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)" mit " *ProductCode*", " *UserSID* " und dem *Kontext* des-Objekts auf. Die Funktions-ID wird als Parameter bereitgestellt.

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

Funktions-ID, die in der Funktions Spalte der [Featuretabelle](feature-table.md)angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der-Befehl erfolgreich ausgeführt wird, enthält die-Eigenschaft den Wert als **DWORD**.



| State                    | Bedeutung                                      |
|--------------------------|----------------------------------------------|
| InstallState \_ angekündigt | Diese Funktion wird angekündigt.                  |
| InstallState \_ lokal      | Das Feature wird lokal installiert.            |
| InstallState- \_ Quelle     | Das Feature wird zum Ausführen von der Quelle installiert. |



 

Wenn der-Befehl fehlschlägt, enthält die-Eigenschaft einen Fehlercode von [**msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Fehler                     | Bedeutung                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler \_ Zugriff \_ verweigert     | Der Aufrufprozess muss über Administratorrechte verfügen, um Informationen zu einem Produkt zu erhalten, das für einen anderen Benutzer als den aktuellen Benutzer installiert ist. |
| Fehler \_ hafte \_ Konfiguration | Die Konfigurationsdaten sind beschädigt.                                                                                                         |
| Fehler bei \_ ungültigem \_ Parameter | An die Funktion wurde ein ungültiger Parameter übergeben.                                                                                           |
| Fehler \_ erfolgreich            | Die Funktion wurde erfolgreich abgeschlossen.                                                                                                       |
| Unbekannter Fehler. \_ \_   | Die Funktions-ID identifiziert keine bekannte Funktion.                                                                                          |
| Unbekannter Fehler. \_ \_   | Der Produktcode identifiziert kein bekanntes Produkt.                                                                                        |
| Fehler bei Fehler \_ Funktion \_   | Unerwarteter interner Fehler.                                                                                                            |



 

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

[**Msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




