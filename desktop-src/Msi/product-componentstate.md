---
description: Die ComponentState-Eigenschaft ist der Installationsstatus der Komponente für die Instanz dieses Produkts. Diese Eigenschaft ruft MsiQueryComponentState mit productCode, UserSid und Context des Objekts auf.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Product.ComponentState-Methode
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
ms.openlocfilehash: d2bc9c5c1f5325dc631f8866ba1a8c7d88ce18d624a2974974f4692bf4f7b067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376779"
---
# <a name="productcomponentstate-method"></a>Product.ComponentState-Methode

Die **ComponentState-Eigenschaft** ist der Installationsstatus der Komponente für die Instanz dieses Produkts.

Diese Eigenschaft ruft [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)mit productCode, UserSid und Context des Objekts auf. Die KOMPONENTEN-ID-GUID wird als Parameter bereitgestellt.

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

Komponentencode-GUID der Komponente, wie in der ComponentID-Spalte der [Component-Tabelle](component-table.md)zu finden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Aufruf erfolgreich ist, enthält die -Eigenschaft den Wert als **DWORD.**



| State                | Bedeutung                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ LOCAL  | Die Komponente wird lokal installiert.                |
| \_INSTALLSTATE-QUELLE | Die Komponente wird installiert, um von der Quelle aus ausgeführt zu werden. |



 

Wenn der Aufruf fehlschlägt, enthält die -Eigenschaft einen Fehlercode aus [**MsiQueryComponentState.**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)



| Fehler                     | Bedeutung                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| FEHLERZUGRIFF \_ \_ VERWEIGERT     | Der aufrufende Prozess muss über Administratorrechte verfügen, um Informationen für einen anderen Benutzer als den aktuellen Benutzer abzurufen. |
| FEHLER: \_ FEHLERHAFTE \_ KONFIGURATION | Die Konfigurationsdaten sind beschädigt.                                                                                 |
| FEHLER: \_ UNGÜLTIGER \_ PARAMETER | Ein ungültiger Parameter wurde an die Funktion übergeben.                                                                   |
| FEHLER \_ ERFOLGREICH            | Die Funktion wurde erfolgreich abgeschlossen.                                                                               |
| \_FEHLER UNBEKANNTE \_ KOMPONENTE | Die Komponenten-ID identifiziert keine bekannte Komponente.                                                              |
| FEHLER \_ \_ UNBEKANNTES PRODUKT   | Der Produktcode identifiziert kein bekanntes Produkt.                                                                |
| \_ \_ FEHLERFUNKTION FEHLGESCHLAGEN   | Ein unerwarteter interner Fehler.                                                                                    |



 

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

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




