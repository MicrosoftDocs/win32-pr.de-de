---
description: Erstellt einen neuen benutzerdefinierten Katalog im Windows Search-Indexer und gibt einen Verweis darauf zurück.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'ISearchManager2:: kreatecatalog-Methode'
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
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214450"
---
# <a name="isearchmanager2createcatalog-method"></a>ISearchManager2:: kreatecatalog-Methode

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

*pszcatalog* \[ in\]
</dt> <dd>

Typ: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Der Name des zu erstellenden Katalogs. Kann ein beliebiger Name sein, der vom Aufrufer ausgewählt wird, darf nur alphanumerische Zeichen und Unterstriche enthalten.

</dd> <dt>

*ppcatalogmanager* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

Bei Erfolg wird ein Verweis auf den erstellten Katalog als [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Schnittstellen Zeiger zurückgegeben. Das Release () muss für diese Schnittstelle aufgerufen werden, nachdem die aufrufende Anwendung die Verwendung der Anwendung abgeschlossen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

HRESULT, das den Status des Vorgangs angibt:



| Rückgabecode                                                                             | Beschreibung                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Katalog war nicht bereits vorhanden und wurde erstellt. Verweis auf den zurückgegebenen Katalog.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Der Katalog war bereits vorhanden, Verweis auf den zurückgegebenen Katalog.<br/>                       |



 

HRESULT-Fehler: Fehler beim Erstellen des Katalogs oder ungültige Argumente.

## <a name="remarks"></a>Bemerkungen

Wird aufgerufen, um einen neuen Katalog im Windows Search-Indexer zu erstellen. Nach der Erstellung können die Methoden im zurückgegebenen [**isearchcatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Manager zum Hinzufügen von zu indizierenden Speicherorten, zum Überwachen des Indizierungs Prozesses und zum Erstellen von Abfragen verwendet werden, die an den Indexer gesendet und Ergebnisse erhalten. Weitere Informationen finden Sie in der Dokumentation zum Verwalten des Indexes: https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
