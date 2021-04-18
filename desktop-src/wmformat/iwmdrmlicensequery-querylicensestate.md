---
title: Iwmdrmlicensequery querylicenerstate-Methode (wmdrmsdk. h)
description: Die querylicenserstate-Methode fragt den lokalen Lizenz Speicher nach Lizenzinformationen ab, die für eine Schlüssel-ID für ein oder mehrere bestimmte Rechte gelten.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Querylicenenstate-Methode Windows Media-Format
- Querylicenserstate-Methode Windows Media-Format, iwmdrmlicensequery-Schnittstelle
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format, querylicenserstate-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372264"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>Iwmdrmlicensequery:: querylicenserstate-Methode

Die **querylicenserstate** -Methode fragt den lokalen Lizenz Speicher nach Lizenzinformationen ab, die für eine Schlüssel-ID für ein oder mehrere bestimmte Rechte gelten.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinkid* \[ in\]
</dt> <dd>

Die Schlüssel-ID, für die abgefragt werden soll. Nur Lizenzen, die auf diese Schlüssel-ID zutreffen, werden ausgewertet.

</dd> <dt>

*cactionstoquery* \[ in\]
</dt> <dd>

Die Anzahl der Aktionen, für die abgefragt werden soll. Dieser Wert muss auf die Anzahl der Elemente in den Arrays festgelegt werden, die für die Parameter *rgbstractionstoquery* und *rgresultstatedata* übermittelt wurden.

</dd> <dt>

*rgbstractionstoquery \[ \]* \[in\]
</dt> <dd>

Ein Array von mindestens einem Recht, für das abgefragt werden soll. Dieses Array muss beliebig viele Elemente enthalten, die von *cactionstoquery* angegeben werden. Jedes Element muss auf eine der folgenden Konstanten festgelegt werden.



| Konstante                                        | BESCHREIBUNG                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszwmdrm \_ licenlstate- \_ Sicherung               | Schließen Sie ein, um die Details zu den rechten zum Sichern und Wiederherstellen der Lizenz abzufragen.                                                               |
| g \_ wszwmdrm \_ licen\state \_ kollaborativeplay    | Schließen Sie ein, um die Details über das Recht zur Freigabe des Inhalts für eine Gruppe von Benutzern im Rahmen eines kollaborativen Wiedergabe Szenarios abzufragen.          |
| "g \_ wszwmdrm \_ licenanstate" \_ Kopieren                 | Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf externe Geräte oder Medien abzufragen.                                                 |
| g \_ wszwmdrm \_ licenanstate \_ copyper CD             | Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf die CD abzufragen.                                                                        |
| g \_ wszwmdrm \_ licensstate \_ copytononsdmidevice  | Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf ein Gerät abzufragen, das die Secure Digital Media Initiative (SDMI) nicht unterstützt. |
| g \_ wszwmdrm \_ \_ licentarstate copytosdmidevice     | Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf ein Gerät abzufragen, das SDMI unterstützt.                                           |
| g \_ wszwmdrm \_ \_ licencstate "erstellungenbnailimage" | Schließen Sie ein, um die Details über das Recht zum Erstellen eines Miniatur Bilds aus dem Inhalt abzufragen.                                                     |
| g \_ wszwmdrm \_ licenanstate- \_ Wiedergabe             | Schließen Sie ein, um die Details über das Recht zur Wiedergabe des Inhalts abzufragen.                                                                              |
| g \_ wszwmdrm \_ licenanstate \_ playlistburn         | Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf CD als Teil einer Wiedergabeliste abzufragen.                                                  |



 

</dd> <dt>

*rgresultstatedata \[ \]* \[out\]
</dt> <dd>

Ein Array aus mindestens einer [**DRM- \_ Lizenz \_ Status \_ Daten**](drmdrm-license-state-data.md) Struktur, die die Lizenz Zustandsinformationen empfängt, die im entsprechenden-Element des *rgbstractionstoquery* -Parameters auf das Recht zutreffen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Lizenzen, die für die angegebene Schlüssel-ID gelten, werden durchsucht und ausgewertet. Die Ergebnisse werden aggregiert, sodass jede **DRM- \_ Lizenz \_ Status- \_ Daten** Strukturinformationen aus mehreren Lizenzen enthalten kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicensequery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





