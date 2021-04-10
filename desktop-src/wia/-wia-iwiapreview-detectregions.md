---
description: 'Ruft den Treiber Segmentierungs Filter auf und übergibt das ungefilterte Bild, das von der iwiapreview:: getnewpreview-Methode zwischengespeichert wird, an den Filter.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: Iwiapreview::D etectregions-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214656"
---
# <a name="iwiapreviewdetectregions-method"></a>Iwiapreview::D etectregions-Methode

Ruft den Treiber Segmentierungs Filter auf und übergibt das ungefilterte Bild, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird, an den Filter.

## <a name="syntax"></a>Syntax


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Nicht verwendet. Auf NULL (0) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Der Vorgang ist erfolgreich.<br/>              |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Der Treiber unterstützt keine Segmentierung.<br/> |
| <dl> <dt>**sonst**</dt> </dl>  | Ein Standard-com-Fehlercode.<br/>                |



 

## <a name="remarks"></a>Bemerkungen

Eine Anwendung muss [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) aufrufen, bevor diese Funktion aufgerufen wird.

Wenn die Windows-Abbild Übernahme (WIA) 2,0 Preview-Komponente **iwiapreview::D etectregions** aufruft, ruft Sie den Treiber Segmentierungs Filter auf und übergibt die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle, die zuvor an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)weitergegeben wurde. Außerdem übergibt Sie das intern zwischengespeicherte Bild an den Filter. Der Segmentierungs Filter verwendet das zwischengespeicherte Bild, um die untergeordneten Blöcke zu erstellen.

Wenn eine Anwendung Eigenschaften der [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle ändert, nachdem Sie [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)aufgerufen hat, müssen die ursprünglichen Eigenschaften wieder hergestellt werden, bevor die Anwendung **iwiapreview::D etectregions** aufruft. Verwenden Sie [**getpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) und [**setpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) , um die ursprünglichen Eigenschaften wiederherzustellen.

**Iwiapreview::D etectregions** wird verwendet, um die "Unterbereiche" des zwischengespeicherten Images zu ermitteln. Für jeden erkannten Unterbereich wird ein neues untergeordnetes WIA 2,0-Element unter der [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle erstellt. Für jedes untergeordnete Element muss der Segmentierungs Filter die Werte für die folgenden WIA 2,0-Eigenschaften festlegen: WIA \_ IPS \_ xpos, WIA \_ IPS \_ yPos, WIA \_ IPS \_ xblock und WIA \_ IPS \_ yblock. Mit einem erweiterten Filter werden andere WIA 2,0-Eigenschaften festgelegt, wie z. b. WIA \_ \_ -IPS deplizierung \_ X und WIA- \_ IPS- \_ deschiefe \_ Y, wenn der Treiber de-Neigung unterstützt. Die WIA \_ \_ -IPS xpos, WIA \_ IPS \_ yPos, WIA \_ IPS \_ xblock und WIA \_ IPS \_ yblock-Eigenschaften stellen das umgebende Rechteck des zu überprüfenden Bereichs dar.

Der Treiber unterstützt möglicherweise keine Segmentierung. Vor dem Aufrufen von **iwiapreview::D etectregions** überprüft eine Anwendung in der Regel, ob der Treiber die WIA- \_ IP- \_ Segmentierungs Eigenschaft unterstützt. Wenn die Eigenschaft nicht implementiert wird, wird die Segmentierung nicht unterstützt, und **iwiapreview::D etectregions** schlägt fehl und gibt E \_ notimpl zurück.

Die Anwendung muss die untergeordneten Elemente bereinigen, die durch Aufrufen von **iwiapreview::D etectregions** erstellt werden. Wenn eine Anwendung z. b. einen zusätzlichen **iwiapreview::D etectregions** für dasselbe Element aufruft, muss Sie die vorherigen untergeordneten Elemente bereinigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




