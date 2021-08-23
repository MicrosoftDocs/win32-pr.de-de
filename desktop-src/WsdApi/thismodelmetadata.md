---
description: Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: thisModelMetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01d074e7e9c8d43e078ebc477366d88608e7c4f3fade6c0be3dbc6fda23f006b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991550"
---
# <a name="thismodelmetadata-element"></a>thisModelMetadata-Element

Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.

## <a name="usage"></a>Verbrauch

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                     | BESCHREIBUNG                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hersteller**](manufacturer.md)<br/>             | Name des Herstellers. Mindestens eine von [**manufacturer oder**](manufacturer.md) [**manufacturerLS**](manufacturerls.md) muss in den Metadaten vorhanden sein.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Lokalisierte Version des Herstellernamens.<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | URL-Adresse des Herstellers.<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | Der Name des Geräts. In den Metadaten [**muss mindestens modelName**](modelname.md) oder [**modelNameLS**](modelnamels.md) vorhanden sein.<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Lokalisierte Version des Gerätenamens.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | Modellnummer des Geräts.<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | URL-Adresse für das Gerätemodell.<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | PnP-X-Kategorie, zu der das Gerät gehört. <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | URL-Adresse der Präsentationsdaten des Gerätemodells.<br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Die Herstellermetadaten sind mit dem Im Geräteprofil beschriebenen Abschnitt mit den Herstellermetadaten (Details finden Sie im Geräteprofil). Der Herstellername oder mindestens eine lokalisierte Version des Herstellernamens muss angegeben werden. Der Modellname oder mindestens eine lokalisierte Version des Modellnamens muss angegeben werden.

Das [**thisModelMetadataDefinition-Element**](thismodelmetadatadefinition.md) wird anschließend verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.

Wenn ein [**PnPXDeviceCategory-Element**](pnpxdevicecategory.md) vorhanden ist, [](hosted.md) muss mindestens ein gehostetes Element sowohl [**PnPXHardwareId-**](pnpxhardwareid.md) als auch [**PnPXCompatibleId-Elemente**](pnpxcompatibleid.md) enthalten. Wenn **PnPXHardwareId-** und **PnPXCompatibleId-Elemente** in  einem gehosteten Element vorhanden sind, muss ein **PnPXDeviceCategory-Element** innerhalb des **thisModelMetadata-Elements** vorhanden sein.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




