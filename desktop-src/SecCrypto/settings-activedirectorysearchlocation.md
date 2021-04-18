---
description: Legt den Active Directory Suchspeicherort fest oder ruft ihn ab.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Settings. activedirectoriysearchlocation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364768"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Settings. activedirectoriysearchlocation (Eigenschaft)

\[Die **activedirector ysearchlocation** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Die **activedirector ysearchlocation** -Eigenschaft legt den Active Directory Suchspeicherort fest oder ruft ihn ab.

## <a name="syntax"></a>Syntax


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der CAPICOM-Enumeration für den [**\_ Active \_ Directory- \_ \_ Suchort**](capicom-active-directory-search-location.md) , der den Such Speicherort angibt. Der Standardwert ist CAPICOM \_ Search \_ any. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                           | Bedeutung                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM- \_ Suche \_ Any**</dt> </dl>                                   | Suchen Sie alle verfügbaren Speicherorte.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**\_ \_ Standard \_ Domäne für CAPICOM-Suche**</dt> </dl> | Nur die Standard Domäne suchen.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM- \_ Suche ( \_ globaler \_ Katalog)**</dt> </dl> | Durchsuchen Sie nur den globalen Katalog.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen**](settings.md)
</dt> </dl>

 

 




