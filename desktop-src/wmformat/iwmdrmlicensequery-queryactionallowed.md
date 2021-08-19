---
title: IWMDRMLicenseQuery QueryActionAllowed-Methode (Wmdrmsdk.h)
description: Die QueryActionAllowed-Methode führt eine Abfrage für den lokalen Lizenzspeicher aus, um den Lizenzstatus für eine oder mehrere DRM-Aktionen abzurufen, die für eine angegebene Schlüssel-ID gelten.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- QueryActionAllowed-Methode windows Media Format
- QueryActionAllowed-Methode windows Media Format , IWMDRMLicenseQuery-Schnittstelle
- IWMDRMLicenseQuery-Schnittstelle windows Media Format , QueryActionAllowed-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f6974a04f92852ef9e56b473126eb8e0cc2d92a9bdcf5192e10abe800978bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846874"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>IWMDRMLicenseQuery::QueryActionAllowed-Methode

Die **QueryActionAllowed-Methode** führt eine Abfrage für den lokalen Lizenzspeicher aus, um den Lizenzstatus für eine oder mehrere DRM-Aktionen abzurufen, die für eine angegebene Schlüssel-ID gelten.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKID* \[ In\]
</dt> <dd>

Schlüssel-ID, für die abgefragt werden soll. Nur Lizenzen, die für diese Schlüssel-ID gelten, werden ausgewertet.

</dd> <dt>

*bstrMinReqIndivVersion* \[ In\]
</dt> <dd>

Die im Header der ASF-Datei angegebene Mindestsicherheitsversion. Dieser Parameter ist optional. Übergeben Sie **NULL,** um die Abfrage ohne diese Informationen auszuführen.

</dd> <dt>

*cActionsToQuery* \[ In\]
</dt> <dd>

Die Anzahl der Aktionen, die abgefragt werden sollen. Dieser Wert muss auf die Anzahl der Elemente in den Arrays festgelegt werden, die für die Parameter *rgbstrActionsToQuery* und *rgdwQueryResult* übergeben werden.

</dd> <dt>

*rgbstrActionsToQuery \[ \]* \[in\]
</dt> <dd>

Array mit mindestens einer Berechtigung, für die abgefragt werden soll. Dieses Array muss so viele Elemente enthalten, wie von *cActionsToQuery* angegeben. Jedes Element muss auf eine der folgenden Konstanten festgelegt werden:



| Konstante                                         | Beschreibung                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ActionAllowed \_ Playback             | Fügen Sie ein, um die Berechtigung zum Wiedergeben des Inhalts abzufragen.                              |
| g \_ wszWMDRM \_ ActionAllowed \_ Copy                 | Schließen Sie ein, um die Berechtigung zum Kopieren des Inhalts auf externe Geräte oder Medien abzufragen. |
| g \_ wszWMDRM \_ ActionAllowed \_ Playlist Überschreiben         | Schließen Sie ein, um die Berechtigung abzufragen, den Inhalt als Teil einer Wiedergabeliste auf CD zu kopieren.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Schließen Sie ein, um die Rechte abzufragen, um ein Miniaturbild aus dem Inhalt zu erstellen.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Fügen Sie ein, um die Berechtigung zum Kopieren des Inhalts auf CD abzufragen.                        |



 

</dd> <dt>

*rgdwQueryResult \[ \]* \[out\]
</dt> <dd>

Array von einer oder mehreren DWORD-Variablen, die die Ergebnisse der Abfrage für die durch *rgbstrActionsToQuery angegebenen* Rechte empfangen. Wenn eine Aktion zulässig ist, wird das entsprechende Element auf 0 (null) festgelegt. Wenn eine Aktion nicht zulässig ist, wird das Element mithilfe des bitweisen OR-Vorgangs auf einen oder mehrere Werte der [**DRM \_ ACTION ALLOWED \_ QUERY \_ \_ RESULTS-Enumeration**](drm-action-allowed-query-results.md) festgelegt. Dieses Array muss so viele Elemente enthalten, wie von *cActionsToQuery* angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie Wiedergabe- und Kopierrechte abfragen, erhalten Sie genauere Ergebnisse, indem Sie zuerst Umgebungsparameter festlegen. Verwenden Sie die [**SetActionAllowedQueryParams-Methode,**](iwmdrmlicensequery-setactionallowedqueryparams.md) um die Umgebungsparameter festzulegen. Die Ergebnisse von Abfragen für das Brandrecht sind von den Umgebungsparametern nicht betroffen. Sie können die Standardwerte sicher verwenden.

Die von der **QueryActionAllowed-Methode** zurückgegebenen Ergebnisse werden aus null oder mehr Lizenzen im lokalen Lizenzspeicher aggregiert. Die -Methode durchsucht möglicherweise nicht alle Lizenzen, die für die Schlüssel-ID gelten, wenn ein aktiviertes Ergebnis auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseQuery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> <dt>

[**Abfragen einfacher Rechteinformationen**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





