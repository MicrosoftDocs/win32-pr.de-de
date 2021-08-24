---
description: Erstellt einen neuen benutzerdefinierten Katalog im Windows Search-Indexer und gibt einen Verweis darauf zurück.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: ISearchManager2::CreateCatalog-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 34a4ceb37045ebbae62e04da0b5395673ed498c56189a26f2abaa376c960c511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597750"
---
# <a name="isearchmanager2createcatalog-method"></a>ISearchManager2::CreateCatalog-Methode

Erstellt einen neuen benutzerdefinierten Katalog im Windows Search-Indexer und gibt einen Verweis darauf zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszCatalog* \[ In\]
</dt> <dd>

Typ: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Name des zu erstellende Katalogs. Kann ein beliebiger vom Aufrufer ausgewählter Name sein, darf nur alphanumerische Standardzeichen und Unterstriche enthalten.

</dd> <dt>

*ppCatalogManager* \[ out\]
</dt> <dd>

Typ: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

Bei Erfolg wird ein Verweis auf den erstellten Katalog als [**ISearchCatalogManager-Schnittstellenzeiger**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) zurückgegeben. Release() muss auf dieser Schnittstelle aufgerufen werden, nachdem die aufrufende Anwendung sie nicht mehr verwendet hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

HRESULT, das den Status des Vorgangs angibt:



| Rückgabecode                                                                             | Beschreibung                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Katalog war zuvor nicht vorhanden und wurde erstellt. Verweis auf den zurückgegebenen Katalog.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Katalog war zuvor vorhanden, Verweis auf den zurückgegebenen Katalog.<br/>                       |



 

FAILED HRESULT: Fehler beim Erstellen eines Katalogs oder übergebene ungültige Argumente.

## <a name="remarks"></a>Hinweise

Wird aufgerufen, um einen neuen Katalog im Windows Search-Indexer zu erstellen. Nach der Erstellung können die Methoden für den zurückgegebenen [**ISearchCatalog-Manager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) verwendet werden, um zu indizierende Standorte hinzuzufügen, den Indizierungsprozess zu überwachen und Abfragen zu erstellen, die an den Indexer gesendet und Ergebnisse abgerufen werden sollen. Weitere Informationen finden Sie in der Dokumentation zum Verwalten des Index: https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
