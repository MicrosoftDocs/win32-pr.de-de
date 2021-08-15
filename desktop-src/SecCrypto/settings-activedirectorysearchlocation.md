---
description: Legt den Active Directory-Suchspeicherort fest oder ruft diese ab.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Einstellungen. ActiveDirectorySearchLocation (Eigenschaft)
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
ms.openlocfilehash: 884866fd5ff6a3e3ff483a255bf2b77063ca81e51141108c9f58fd45629cc036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900320"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Einstellungen. ActiveDirectorySearchLocation (Eigenschaft)

\[Die **ActiveDirectorySearchLocation-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.\]

Die **ActiveDirectorySearchLocation-Eigenschaft** legt den Active Directory-Suchspeicherort fest oder ruft den Suchspeicherort ab.

## <a name="syntax"></a>Syntax


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ ACTIVE DIRECTORY SEARCH \_ \_ \_ LOCATION-Enumeration,**](capicom-active-directory-search-location.md) der den Suchspeicherort angibt. Der Standardwert ist CAPICOM \_ SEARCH \_ ANY. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                           | Bedeutung                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM \_ SEARCH \_ ANY**</dt> </dl>                                   | Durchsuchen Sie alle verfügbaren Standorte.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**CAPICOM \_ \_ SEARCH-STANDARDDOMÄNE \_**</dt> </dl> | Durchsuchen Sie nur die Standarddomäne.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM \_ SEARCH \_ GLOBAL \_ CATALOG**</dt> </dl> | Durchsuchen Sie nur den globalen Katalog.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Einstellungen**](settings.md)
</dt> </dl>

 

 




