---
description: Diese Elemente bilden das XML-Schema, das im Webpublishing-und Online-Assistenten für das Drucken von Druck Reihen verwendet wird.
title: Schema des Übertragungs Manifests
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994942"
---
# <a name="transfer-manifest-schema"></a>Schema des Übertragungs Manifests

Diese Elemente bilden das XML-Schema, das im Webpublishing-und Online-Assistenten für das Drucken von Druck Reihen verwendet wird.

Die folgenden Elemente sind für das Übertragungs Manifest definiert.

-   [cancelledpage](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [failurepage](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Ort](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [datei](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [FileList](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [Pfalz](#syntax)
    -   [Syntax](#syntax)
    -   [Attribute](#attributes)
    -   [Elementinformationen](#element-information)
-   [folderlist](#syntax)
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
-   [ImageProperty](#syntax)
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
-   [erfolgreicher Dienst](#syntax)
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
-   [UploadInfo](#syntax)
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
| [UploadInfo](#syntax) | Keine           |



 

## <a name="failurepage"></a>failurepage

Gibt die serverseitige HTML-Seite an, die angezeigt wird, wenn der Upload nicht erfolgreich ist.

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
| href      | Erforderlich. Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Upload nicht erfolgreich ist. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [UploadInfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="favorite"></a>speichern

Weist den Assistenten an, einen Favoriten Website Eintrag im Menü " **Favoriten** " für die angegebene URL zu erstellen. Wenn dieses Element nicht angegeben ist, wird das [htmlui](#syntax) -Element an seiner Stelle verwendet.

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
| comment   | Erforderlich. Der Kommentar, der dem **Favoriten** Eintrag zugeordnet ist.         |
| href      | Erforderlich. Die URL des **Favoriten** Eintrags.                          |
| name      | Erforderlich. Der Name für die URL, die im Menü " **Favoriten** " angezeigt wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [UploadInfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="file"></a>file

Beschreibt eine einzelne Datei, die kopiert werden soll. Mehrere [Datei](#syntax) Elemente können unter einem einzelnen [FileList](#syntax) -Knoten enthalten sein.

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
| ContentType | Optional. Der MIME-Typ der Datei.                                                                                                                                         |
| destination | Erforderlich. Ein empfohlener Pfad für die Datei, nachdem Sie hochgeladen wurde. Dieser Pfad ist relativ zur Ziel-URL der uploadwebsite. Der uploadstandort kann diesen Wert nach Bedarf ändern. |
| Erweiterung   | Optional. Die Dateinamenerweiterung der Datei.                                                                                                                               |
| id          | Erforderlich. Der numerische Index der Datei.                                                                                                                                   |
| size        | Optional. Die Größe der Datei (in Bytes).                                                                                                                                    |
| source      | Erforderlich. Der vollständige Dateisystempfad für die Datei.                                                                                                                            |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element      | Untergeordnete Elemente                                          |
|---------------------|---------------------------------------------------------|
| [FileList](#syntax) | [Metadaten](#syntax), [Post](#syntax), [Größe ändern](#syntax) |



 

## <a name="filelist"></a>FileList

Ein Container für-Elemente, die die zu kopierenden Dateien beschreiben. Mehrere [FileList](#syntax) -Elemente können unter einem einzelnen [transfermanifest](#syntax) -Knoten enthalten sein.

### <a name="syntax"></a>Syntax


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>Attribute



| attribute   | BESCHREIBUNG      |
|-------------|------------------|
| Einsatz Ordner | Nicht implementiert. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element              | Untergeordnete Elemente  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [datei](#syntax) |



 

## <a name="folder"></a>folder

Beschreibt einen Ordner, in dem Dateien gespeichert werden. Mehrere [Ordner](#syntax) Elemente können unter einem einzelnen [folderlist](#syntax) -Knoten enthalten sein.

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
| destination | Erforderlich. Ein empfohlener Pfad für den Ordner, nachdem er hochgeladen wurde. Dieser Pfad ist relativ zur Ziel-URL der uploadwebsite. Der uploadstandort kann diesen Wert nach Bedarf ändern. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente |
|-----------------------|----------------|
| [folderlist](#syntax) | Keine           |



 

## <a name="folderlist"></a>folderlist

Ein Container für-Elemente, die die zu kopierenden Dateien beschreiben. Mehrere [folderlist](#syntax) -Elemente können unter einem einzelnen [transfermanifest](#syntax) -Knoten enthalten sein.

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
| [transfermanifest](#syntax) | [Pfalz](#syntax) |



 

## <a name="formdata"></a>formdata

Beschreibt optionale HTML-codierte Formulardaten, die mit den Dateien übertragen werden können. Dieses Element wird vom-Dienst hinzugefügt, wenn es für das Hochladen der Dateien als mehrteilige Post-Bereitstellung entscheidet. Die Formulardaten werden sowie Informationen aus dem [Post](#syntax) -Element verwendet, um den Post-Header zu erstellen.

Unter einem einzelnen [UploadInfo](#syntax) -Knoten können mehrere [formdata](#syntax) -Elemente enthalten sein.

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
| name      | Erforderlich. Definiert den Formulardaten Namen, der diesem Abschnitt des Uploads zugeordnet ist. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente |
|-----------------------|----------------|
| [UploadInfo](#syntax) | Keine           |



 

## <a name="htmlui"></a>htmlui

Die URL der serverseitigen HTML-Seite, die angezeigt wird, wenn der Assistent geschlossen wird. Dieses Element erstellt einen bevorzugten webseiteneintrag im Menü " **Favoriten** ", wenn das [bevorzugte](#syntax) Element fehlt und der Anzeige Name der uploadwebsite angegeben wird.

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
| [UploadInfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="imageproperty"></a>ImageProperty

Gibt eine Bild Eigenschaft in Bezug auf die Datei an. Mehrere [ImageProperty](#syntax) -Elemente können unter einem einzelnen [Metadatenknoten](#syntax) enthalten sein.

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

Ein Container für Elemente und Text, die Metadaten für die jeweilige Datei definieren. Mehrere [Metadatenelemente](#syntax) können unter einem einzelnen [Datei](#syntax) Knoten enthalten sein.

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
| [datei](#syntax) | [ImageProperty](#syntax) |



 

## <a name="netplace"></a>netplace

Definiert das Ziel für einen Netzwerk Speicherort, der nach Abschluss des Uploads an den **Netzwerk Orten** erstellt wird. Die Erstellung eines Netzwerk Orts kann durch die [**ipublishingwizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) -Methode verhindert werden.

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
| comment   | Erforderlich. Der Kommentar, der für das Netzwerk Platz Symbol angezeigt wird, wenn der Cursor darauf liegt.         |
| href      | Erforderlich. Die URL des Netzwerk Orts Eintrags.                                                   |
| name      | Erforderlich. Der Name für das Symbol für den Netzwerk Platz, der im Ordner " **meine Netzwerk Orte** " angezeigt wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [UploadInfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="post"></a>post

Die URL, zu der die Datei gepostet werden soll. Dieses Element wird vom-Dienst hinzugefügt, wenn die Übertragung als mehrteilige Post-Übermittlung erfolgt und mit [formdata](#syntax)verwendet wird, um den Post-Header zu erstellen. Wenn der Dienst die Dateiübertragung mithilfe World Wide Web verteilten Erstellungs-und Versionsverwaltung (WebDAV) durchführen möchte, sollte dieses Element nicht hinzugefügt werden. Mehrere [Post](#syntax) -Elemente können unter einem einzelnen [Datei](#syntax) Knoten enthalten sein.

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
| href      | Erforderlich. Die URL des Ziel Ordners.                                   |
| name      | Erforderlich. Definiert den Formulardaten Namen, der diesem Abschnitt des Beitrags zugeordnet ist. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element  | Untergeordnete Elemente      |
|-----------------|---------------------|
| [datei](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>resize

Definiert die Skalierung und Neukomprimierung einer Bilddatei in das JPEG-Format. Wenn die Quelldatei bereits im JPEG-Format vorliegt und kleiner oder gleich der angegebenen Breite und Höhe ist, wird Sie nicht skaliert. Wenn die Quelldatei keine JPEG-Datei ist, wird Sie konvertiert. Die Skalierung, Neukomprimierung und Konvertierung der Datei kann durch die [**ipublishingwizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) -Methode verhindert werden. Mehrere Elemente zur [Größenänderung](#syntax) können unter einem einzelnen [Datei](#syntax) Knoten enthalten sein.

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
| verschoben        | Erforderlich. Die Breite des Bilds nach dem Hochladen in Pixel. Wenn dieser Wert 0 ist, wird **CX** aus dem **CY** -Wert berechnet, um relative Dimensionen beizubehalten.  |
| cy        | Erforderlich. Die Höhe des Bilds nach dem Hochladen in Pixel. Wenn dieser Wert 0 ist, wird **CY** aus dem **CX** -Wert berechnet, um relative Dimensionen beizubehalten. |
| Qualität   | Erforderlich. Der Wert der JPEG-Qualität zwischen 0 und 100, wobei 100 die höchste Qualität ist.                                                                            |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element  | Untergeordnete Elemente |
|-----------------|----------------|
| [datei](#syntax) | Keine.          |



 

## <a name="successpage"></a>erfolgreicher Dienst

Gibt die serverseitige HTML-Seite an, die angezeigt wird, wenn der Upload erfolgreich ist.

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
| href      | Erforderlich. Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Upload erfolgreich ist. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [UploadInfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="target"></a>target

Ein Zielordner, der im UNC-Format (Universal Naming Convention) oder als WebDAV-Server angegeben ist. Der Dienst fügt dieses Ziel hinzu, um einen Zielordner anzugeben, wenn für die Übertragung ein WebDAV-oder Dateisystem Protokoll verwendet wird. Wenn der Dienst die Dateiübertragung als mehrteiligen Beitrag ausführt, sollte er dieses Element nicht hinzufügen.

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
| href      | Erforderlich. Die URL des Ziel Ordners. Verwenden Sie das **https://** -Formular für WebDAV oder das **\\ \\ Server \\ Freigabe** Formular für UNC. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element        | Untergeordnete Elemente         |
|-----------------------|------------------------|
| [UploadInfo](#syntax) | Keine. Text ist zulässig. |



 

## <a name="transfermanifest"></a>transfermanifest

Der übergeordnete Knoten der Datei des Übertragungs Manifests.

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
| Keine           | [FileList](#syntax), [folderlist](#syntax), [UploadInfo](#syntax) |



 

## <a name="uploadinfo"></a>UploadInfo

Ein Container für-Elemente, die Informationen von der in der Transaktion verwendeten uploadwebsite bereitstellen. Mehrere [UploadInfo](#syntax) -Elemente können unter einem einzelnen [transfermanifest](#syntax) -Knoten enthalten sein.

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
| FriendlyName | Erforderlich. Ein Anzeige Name für die Website, der im Assistenten angezeigt wird. |



 

### <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element              | Untergeordnete Elemente                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [Favorit](#syntax), [htmlui](#syntax), [netplace](#syntax), [erfolgreicher spage](#syntax), [target](#syntax) |



 

 

 



