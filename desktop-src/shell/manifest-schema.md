---
description: Diese Elemente bilden das XML-Schema, das im Übertragungsmanifest des Assistenten für Webveröffentlichung und Onlinedruckreihenfolge verwendet wird.
title: Übertragen des Manifestschemas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 30324e32e1bd841423318a37eb1472d673ffc53c6e745f54f9398cec73138239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858856"
---
# <a name="transfer-manifest-schema"></a>Übertragen des Manifestschemas

Diese Elemente bilden das XML-Schema, das im Übertragungsmanifest des Assistenten für Webveröffentlichung und Onlinedruckreihenfolge verwendet wird.

Die folgenden Elemente werden für das Übertragungsmanifest definiert.

-   [cancelledpage](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [failurepage](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Lieblings-](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [datei](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Liste](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Ordner](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Ordnerliste](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [formdata](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [htmlui](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [imageproperty](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [metadata](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [netplace](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Bereitstellen](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Größe](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Successpage](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Ziel](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [transfermanifest](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [uploadinfo](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)

## <a name="cancelledpage"></a>cancelledpage

Gibt die serverseitige HTML-Seite an, die angezeigt werden soll, bevor der Assistent geschlossen wird, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.

### <a name="syntax"></a>Syntax


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| href      | Erforderlich. Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Keine           |



 

## <a name="failurepage"></a>failurepage

Gibt die serverseitige HTML-Seite an, die angezeigt werden soll, wenn der Upload nicht erfolgreich war.

### <a name="syntax"></a>Syntax


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| href      | Erforderlich. Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Upload nicht erfolgreich war. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="favorite"></a>speichern

Weist den Assistenten an, einen Favoriteneintrag für die Website im Menü **Favoriten** für die angegebene URL zu erstellen. Wenn dieses Element nicht angegeben ist, wird das [htmlui-Element](#syntax) an seiner Stelle verwendet.

### <a name="syntax"></a>Syntax


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                            |
|-----------|------------------------------------------------------------------------|
| comment   | Erforderlich. Der kommentar, der dem Eintrag **Favoriten** zugeordnet ist.         |
| href      | Erforderlich. Die URL des **Eintrags Favoriten.**                          |
| name      | Erforderlich. Der Name der URL, die im Menü **Favoriten** angezeigt wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="file"></a>file

Beschreibt eine einzelne Datei, die kopiert werden soll. Mehrere [Dateielemente](#syntax) können in einem einzelnen [Dateilistenknoten](#syntax) enthalten sein.

### <a name="syntax"></a>Syntax


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute   | BESCHREIBUNG                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contenttype | Optional. Der MIME-Typ der Datei.                                                                                                                                         |
| destination | Erforderlich. Ein vorgeschlagener Pfad für die Datei, nachdem sie hochgeladen wurde. Dieser Pfad ist relativ zur Ziel-URL der Uploadwebsite. Die Uploadwebsite kann diesen Wert bei Bedarf ändern. |
| Erweiterung   | Optional. Die Dateinamenerweiterung der Datei.                                                                                                                               |
| id          | Erforderlich. Der numerische Index der Datei.                                                                                                                                   |
| Größe        | Optional. Die Größe der Datei (in Bytes).                                                                                                                                    |
| source      | Erforderlich. Der vollständige Dateisystempfad für die Datei.                                                                                                                            |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element      | Untergeordnete Elemente                                          |
|---------------------|---------------------------------------------------------|
| [Liste](#syntax) | [Metadata](#syntax), [post](#syntax), [resize](#syntax) |



 

## <a name="filelist"></a>Liste

Ein Container für Elemente, die die zu kopierenden Dateien beschreiben. Mehrere [Filelist-Elemente](#syntax) können unter einem einzelnen [transfermanifest-Knoten](#syntax) enthalten sein.

### <a name="syntax"></a>Syntax


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute   | Beschreibung      |
|-------------|------------------|
| usesfolders | Nicht implementiert. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element              | Untergeordnete Elemente  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [datei](#syntax) |



 

## <a name="folder"></a>folder

Beschreibt einen Ordner, in dem Dateien gespeichert werden. Mehrere [Ordnerelemente](#syntax) können in einem einzelnen [Ordnerlistenknoten](#syntax) enthalten sein.

### <a name="syntax"></a>Syntax


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a>Attribute



| attribute   | Beschreibung                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination | Erforderlich. Ein vorgeschlagener Pfad für den Ordner, nachdem er hochgeladen wurde. Dieser Pfad ist relativ zur Ziel-URL der Uploadwebsite. Die Uploadwebsite kann diesen Wert bei Bedarf ändern. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente |
|-----------------------|----------------|
| [Ordnerliste](#syntax) | Keine           |



 

## <a name="folderlist"></a>Ordnerliste

Ein Container für Elemente, die die zu kopierenden Dateien beschreiben. Mehrere [Ordnerlistenelemente](#syntax) können unter einem einzelnen [transfermanifest-Knoten](#syntax) enthalten sein.

### <a name="syntax"></a>Syntax


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>Attribute

Keine

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element              | Untergeordnete Elemente    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [Ordner](#syntax) |



 

## <a name="formdata"></a>formdata

Beschreibt optionale HTML-codierte Formulardaten, die mit den Dateien übertragen werden können. Dieses Element wird vom Dienst hinzugefügt, wenn er sich dafür auswählt, die Dateien als mehrteiligen Beitrag hochzuladen. Die Formulardaten werden zusammen mit Informationen aus dem [post-Element](#syntax) verwendet, um den Postheader zu erstellen.

Mehrere [formdata-Elemente](#syntax) können in einem einzelnen [uploadinfo-Knoten enthalten](#syntax) sein.

### <a name="syntax"></a>Syntax


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                      |
|-----------|----------------------------------------------------------------------------------|
| name      | Erforderlich. Definiert den Formulardatennamen, der diesem Abschnitt des Uploads zugeordnet ist. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Keine           |



 

## <a name="htmlui"></a>htmlui

Die URL der serverseitigen HTML-Seite, die angezeigt wird, wenn der Assistent geschlossen wird. Dieses Element erstellt einen favoriten Webseiteneintrag [](#syntax) im **Menü Favoriten,** wenn das Favoritenelement nicht vorhanden ist und der Benutzerfreundlichname der Uploadwebsite angegeben ist.

### <a name="syntax"></a>Syntax


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| href      | Erforderlich. Die URL der serverseitigen HTML-Seite, die angezeigt wird, wenn der Assistent geschlossen wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="imageproperty"></a>imageproperty

Gibt eine Bildeigenschaft im Zusammenhang mit der Datei an. Mehrere [imageproperty-Elemente](#syntax) können in einem einzelnen [Metadatenknoten enthalten](#syntax) sein.

### <a name="syntax"></a>Syntax


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                  |
|-----------|----------------------------------------------|
| id        | Erforderlich. Die ID der bestimmten Eigenschaft. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element      | Untergeordnete Elemente         |
|---------------------|------------------------|
| [metadata](#syntax) | Keine. Text ist zulässig. |



 

## <a name="metadata"></a>metadata

Ein Container für Elemente und Text, der Metadaten für die bestimmte Datei definiert. Mehrere [Metadatenelemente](#syntax) können unter einem einzelnen [Dateiknoten enthalten](#syntax) sein.

### <a name="syntax"></a>Syntax


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>Attribute

Keine

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element  | Untergeordnete Elemente           |
|-----------------|--------------------------|
| [datei](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>netplace

Definiert das Ziel für einen Netzwerkort, der nach Abschluss des Uploads unter **Meine Netzwerkorte** erstellt wird. Die Erstellung eines Netzwerkplatzes kann mit der [**IPublishingWizard::Initialize-Methode verhindert**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) werden.

### <a name="syntax"></a>Syntax


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| comment   | Erforderlich. Der Kommentar, der für das Symbol für den Netzwerkplatz angezeigt wird, wenn der Cursor darauf ruht.         |
| href      | Erforderlich. Die URL des Eintrags für den Netzwerkplatz.                                                   |
| name      | Erforderlich. Der Name für das Symbol für den Netzwerkspeicherort, das im Ordner **Meine Netzwerkorte angezeigt** wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="post"></a>post

URL, an die die Datei gesendet werden soll. Dieses Element wird vom Dienst hinzugefügt, wenn die Übertragung als mehrteilige Post erfolgt und mit [formdata](#syntax)verwendet wird, um den Postheader zu erstellen. Wenn der Dienst die Dateiübertragung mithilfe von World Wide Web Distributed Authoring and Versioning (WebDAV) auswählt, sollte er dieses Element nicht hinzufügen. Mehrere [Post-Elemente](#syntax) können in einem einzelnen [Dateiknoten enthalten](#syntax) sein.

### <a name="syntax"></a>Syntax


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute | Beschreibung                                                                    |
|-----------|--------------------------------------------------------------------------------|
| Dateiname  | Optional. Der Dateiname für die gepostete Datei.                                   |
| href      | Erforderlich. Die URL des Zielordners.                                   |
| name      | Erforderlich. Definiert den Formulardatennamen, der diesem Abschnitt des Beitrags zugeordnet ist. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element  | Untergeordnete Elemente      |
|-----------------|---------------------|
| [datei](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>resize

Definiert die Skalierung und Neukomprimierung einer Bilddatei im JPEG-Format. Wenn die Quelldatei bereits im JPEG-Format vorliegt und kleiner oder gleich der angegebenen Breite und Höhe ist, ist sie nicht dimensionierend. Wenn die Quelldatei keine JPEG-Datei ist, wird sie konvertiert. Skalierung, Neukomprimierung und Konvertierung der Datei können über die [**IPublishingWizard::Initialize-Methode**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) verhindert werden. Mehrere [Größenänderungselemente](#syntax) können in einem einzelnen [Dateiknoten](#syntax) enthalten sein.

### <a name="syntax"></a>Syntax


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cx        | Erforderlich. Die Breite des Bilds in Pixel nach dem Hochladen. Wenn dieser Wert 0 ist, wird **cx** anhand des **Cy-Werts** berechnet, um relative Dimensionen beizubehalten.  |
| cy        | Erforderlich. Die Höhe des Bilds in Pixel nach dem Hochladen. Wenn dieser Wert 0 ist, wird **cy** anhand des **cx-Werts** berechnet, um relative Dimensionen beizubehalten. |
| Qualität   | Erforderlich. Der JPEG-Qualitätswert zwischen 0 und 100, wobei 100 die höchste Qualität ist.                                                                            |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element  | Untergeordnete Elemente |
|-----------------|----------------|
| [datei](#syntax) | Keine.          |



 

## <a name="successpage"></a>Successpage

Gibt die serverseitige HTML-Seite an, die angezeigt werden soll, wenn der Upload erfolgreich war.

### <a name="syntax"></a>Syntax


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| href      | Erforderlich. Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Upload erfolgreich war. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="target"></a>target

Ein Zielordner, der im UNC-Format (Universal Naming Convention) oder als WebDAV-Server angegeben ist. Der Dienst fügt dieses Ziel hinzu, um einen Zielordner anzugeben, wenn bei der Übertragung ein WebDAV- oder Dateisystemprotokoll verwendet wird. Wenn der Dienst die Dateiübertragung als mehrteiligen Beitrag ausführt, sollte er dieses Element nicht hinzufügen.

### <a name="syntax"></a>Syntax


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| href      | Erforderlich. Die URL des Zielordners. Verwenden Sie das **formular https://** für WebDAV oder das Formular für die **\\ \\ \\ Serverfreigabe** für UNC. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="transfermanifest"></a>transfermanifest

Der übergeordnete Knoten der Übertragungsmanifestdatei.

### <a name="syntax"></a>Syntax


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>Attribute

Keine

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element | Untergeordnete Elemente                                                    |
|----------------|-------------------------------------------------------------------|
| Keine           | [filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Ein Container für Elemente, die Informationen von der upload-Website bereitstellen, die in der Transaktion verwendet wird. Mehrere [uploadinfo-Elemente](#syntax) können unter einem einzelnen [transfermanifest-Knoten](#syntax) enthalten sein.

### <a name="syntax"></a>Syntax


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a>Attribute



| attribute    | BESCHREIBUNG                                                                 |
|--------------|-----------------------------------------------------------------------------|
| friendlyname | Erforderlich. Ein Anzeigename für die Website, der im Assistenten angezeigt wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element              | Untergeordnete Elemente                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax) |



 

 

 



