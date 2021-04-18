---
description: Die componentstate-Eigenschaft ist der Installationsstatus der Komponente für die Instanz dieses Produkts. Diese Eigenschaft ruft msiquerycomponentstate mit ProductCode, UserSID und Kontext des-Objekts auf.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Product. componentstate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365535"
---
# <a name="productcomponentstate-method"></a>Product. componentstate-Methode

Die **componentstate** -Eigenschaft ist der Installationsstatus der Komponente für die Instanz dieses Produkts.

Diese Eigenschaft ruft [**msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)mit ProductCode, UserSID und Kontext des-Objekts auf. Die Komponenten-ID-GUID wird als Parameter bereitgestellt.

## <a name="syntax"></a>Syntax


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* 
</dt> <dd>

Komponenten Code-GUID der Komponente, wie Sie in der ComponentID-Spalte der [Component-Tabelle](component-table.md)gefunden wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der-Befehl erfolgreich ausgeführt wird, enthält die-Eigenschaft den Wert als **DWORD**.



| State                | Bedeutung                                            |
|----------------------|----------------------------------------------------|
| InstallState \_ lokal  | Die Komponente wird lokal installiert.                |
| InstallState- \_ Quelle | Die Komponente wird zum Ausführen von der Quelle installiert. |



 

Wenn der-Befehl fehlschlägt, enthält die-Eigenschaft einen Fehlercode aus [**msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Fehler                     | Bedeutung                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| Fehler \_ Zugriff \_ verweigert     | Der Aufrufprozess muss über Administratorrechte verfügen, um Informationen für einen anderen Benutzer als den aktuellen Benutzer zu erhalten. |
| Fehler \_ hafte \_ Konfiguration | Die Konfigurationsdaten sind beschädigt.                                                                                 |
| Fehler bei \_ ungültigem \_ Parameter | An die Funktion wurde ein ungültiger Parameter übergeben.                                                                   |
| Fehler \_ erfolgreich            | Die Funktion wurde erfolgreich abgeschlossen.                                                                               |
| \_unbekannter Fehler \_ Komponente. | Die Komponenten-ID identifiziert keine bekannte Komponente.                                                              |
| Unbekannter Fehler. \_ \_   | Der Produktcode identifiziert kein bekanntes Produkt.                                                                |
| Fehler bei Fehler \_ Funktion \_   | Unerwarteter interner Fehler.                                                                                    |



 

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

[**Msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




