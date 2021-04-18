---
title: Iwmdrmlicensequery queryaktionallowed-Methode (wmdrmsdk. h)
description: Die queryaktionallowed-Methode führt eine Abfrage für den lokalen Lizenz Speicher aus, um den Lizenzstatus für mindestens eine DRM-Aktion abzurufen, die auf eine angegebene Schlüssel-ID angewendet wird.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Queryaktionallowed-Methode Windows Media-Format
- Queryaktionallowed-Methode, Windows Media-Format, iwmdrmlicensequery-Schnittstelle
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format, queryaktionallowed-Methode
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
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358137"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>Iwmdrmlicensequery:: queryaktionallowed-Methode

Die **queryaktionallowed** -Methode führt eine Abfrage für den lokalen Lizenz Speicher aus, um den Lizenzstatus für mindestens eine DRM-Aktion abzurufen, die auf eine angegebene Schlüssel-ID angewendet wird.

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

*bstrinkid* \[ in\]
</dt> <dd>

Die Schlüssel-ID, für die abgefragt werden soll. Nur Lizenzen, die auf diese Schlüssel-ID zutreffen, werden ausgewertet.

</dd> <dt>

*bstrauminreqindivversion* \[ in\]
</dt> <dd>

Die minimale Sicherheitsversion, die im-Header der ASF-Datei angegeben ist. Dieser Parameter ist optional. Übergeben Sie **null** , um die Abfrage ohne diese Informationen auszuführen.

</dd> <dt>

*cactionstoquery* \[ in\]
</dt> <dd>

Die Anzahl der Aktionen, für die abgefragt werden soll. Dieser Wert muss auf die Anzahl der Elemente in den Arrays festgelegt werden, die für die Parameter *rgbstractionstoquery* und *rgdwqueryresult* übersprungen werden.

</dd> <dt>

*rgbstractionstoquery \[ \]* \[in\]
</dt> <dd>

Ein Array von mindestens einem Recht, für das abgefragt werden soll. Dieses Array muss beliebig viele Elemente enthalten, die von *cactionstoquery* angegeben werden. Jedes Element muss auf eine der folgenden Konstanten festgelegt werden:



| Konstante                                         | BESCHREIBUNG                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszwmdrm- \_ Wiedergabe, Aktions zulässig \_             | Einschließen, um das Recht zum Wiedergeben des Inhalts abzufragen.                              |
| g \_ wszwmdrm- \_ Aktions zulässige \_ Kopie                 | Schließen Sie ein, um das Recht zum Kopieren des Inhalts auf externe Geräte oder Medien zu Fragen. |
| g \_ wszwmdrm \_ Action Allowed \_ playlistburn         | Schließen Sie ein, um das Recht zum Kopieren des Inhalts als Teil einer Wiedergabeliste auf CD zu Fragen.  |
| g \_ wszwmdrm- \_ Aktions zulässig ( \_ "") "". | Schließen Sie zum Abfragen der Berechtigung ein, um ein Miniaturbild aus dem Inhalt zu erstellen.     |
| g \_ wszwmdrm- \_ Aktions zulässige \_ copyper-CD             | Schließen Sie ein, um das Recht zum Kopieren des Inhalts auf die CD abzufragen.                        |



 

</dd> <dt>

*rgdwqueryresult \[ \]* \[out\]
</dt> <dd>

Ein Array von mindestens einer DWORD-Variablen, die die Ergebnisse der Abfrage für die durch *rgbstractionstoquery* angegebenen Rechte empfangen. Wenn eine Aktion zulässig ist, wird das entsprechende Element auf 0 (null) festgelegt. Wenn eine Aktion unzulässig ist, wird das-Element auf einen oder mehrere Werte der DRM- [**\_ Aktion \_ zulässige \_ Abfrage \_ Ergebnis**](drm-action-allowed-query-results.md) Enumeration in Kombination mit dem bitweisen OR-Vorgang festgelegt. Dieses Array muss beliebig viele Elemente enthalten, die von *cactionstoquery* angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Beim Abfragen von Wiedergabe-und Kopier rechten erhalten Sie genauere Ergebnisse, indem Sie zuerst die Umgebungsparameter festlegen. Legen Sie die Umgebungsparameter mit der [**setactionzugewiesene wedqueryparams**](iwmdrmlicensequery-setactionallowedqueryparams.md) -Methode fest. Die Ergebnisse von Abfragen für das Brennrecht sind von den Umgebungs Parametern nicht betroffen. Sie können die Standardeinstellungen sicher verwenden.

Die von der **queryaktionallowed** -Methode zurückgegebenen Ergebnisse werden von 0 (null) oder mehr Lizenzen im lokalen Lizenz Speicher aggregiert. Die-Methode durchsucht möglicherweise nicht alle Lizenzen, die für die Schlüssel-ID gelten, wenn Sie auf ein aktiviertes Ergebnis stößt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicensequery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> <dt>

[**Abfragen von einfachen Rechte Informationen**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





