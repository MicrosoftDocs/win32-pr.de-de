---
description: Definiert die Hersteller-und Modell Metadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: thismodelmetadata-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867600"
---
# <a name="thismodelmetadata-element"></a>thismodelmetadata-Element

Definiert die Hersteller-und Modell Metadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.

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
| [**Bauers**](manufacturer.md)<br/>             | Der Name des Herstellers. In den Metadaten muss mindestens einer der [**Hersteller**](manufacturer.md) oder [**manufacturerls**](manufacturerls.md) vorhanden sein.<br/> <br/> |
| [**manufacturerls**](manufacturerls.md)<br/>         | Lokalisierte Version des Hersteller namens.<br/> <br/>                                                                                                                 |
| [**ManufacturerUrl**](manufacturerurl.md)<br/>       | Die URL-Adresse des Herstellers.<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | Der Name des Geräts. In den Metadaten muss mindestens eine von [**modelname**](modelname.md) oder [**modelnamels**](modelnamels.md) vorhanden sein.<br/> <br/>                   |
| [**modelnamels**](modelnamels.md)<br/>               | Lokalisierte Version des Geräte namens.<br/> <br/>                                                                                                                       |
| [**modelnumber**](modelnumber.md)<br/>               | Modellnummer des Geräts.<br/> <br/>                                                                                                                                 |
| [**modelurl**](modelurl.md)<br/>                     | Die URL-Adresse für das Gerätemodell.<br/> <br/>                                                                                                                           |
| [**Pnpxde vicecategory**](pnpxdevicecategory.md)<br/> | PnP-X-Kategorie, zu der das Gerät gehört. <br/> <br/>                                                                                                                |
| [**presentationurl**](presentationurl.md)<br/>       | Die URL-Adresse der Präsentationsdaten des Geräte Modells.<br/> <br/>                                                                                                        |



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
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Hersteller Metadaten stimmen mit dem im Geräte Profil beschriebenen Abschnitt der Hersteller Metadaten überein (Weitere Informationen finden Sie im Geräte Profil). Der Herstellername oder mindestens eine lokalisierte Version des Hersteller namens muss angegeben werden. Der Modellname oder mindestens eine lokalisierte Version des Modell namens muss angegeben werden.

Anschließend wird das [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) -Element verwendet, um eine C-Konstante zu generieren, die diese Informationen enthält.

Wenn ein [**pnpxenvicecategory**](pnpxdevicecategory.md) -Element vorhanden ist, muss mindestens ein [**gehosteter**](hosted.md) -Element sowohl [**pnpxhardwareid**](pnpxhardwareid.md) -als auch [**pnpxcompatibleid-**](pnpxcompatibleid.md) Elemente enthalten. Ebenso muss, wenn **pnpxhardwareid** -und **pnpxcompatibleid-** Elemente in einem **gehosteten** Element vorhanden sind, ein **pnpxenvicecategory** -Element im **thismodelmetadata** -Element vorhanden sein.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




