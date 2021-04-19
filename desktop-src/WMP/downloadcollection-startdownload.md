---
title: Download Collection. startDownload-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die startDownload-Methode fügt einen Download zur Warteschlange.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- startDownload-Methode, Windows-Media Player
- startDownload-Methode, Windows Media Player, downloadcollection-Klasse
- Download Collection-Klasse, Windows Media Player, startDownload-Methode
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370273"
---
# <a name="downloadcollectionstartdownload-method"></a>Download Collection. startDownload-Methode

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **startDownload** -Methode fügt einen Download zur Warteschlange.

## <a name="syntax"></a>Syntax


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SourceUrl* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die URL des Downloads angibt.

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Typ des Downloads angibt. Enthält einen der folgenden Werte.



| Wert      | BESCHREIBUNG                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP und höher.) Der Download erfolgt als Hintergrundprozess, wenn die Prozessorzeit verfügbar wird. Download Zustände bleiben auch dann erhalten, wenn Windows Media Player oder Windows XP heruntergefahren wird. |
| Echt Zeit  | (Alle unterstützten Betriebssysteme) Der Download erfolgt alle auf einmal. Zwischen den Sitzungen bleiben keine Download Zustände erhalten.                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein-Objekt vom Typ " **Downloader** " zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein neuer Download gestartet wird, fügt der Download-Manager ihn als Element der Download Sammlung hinzu, die den Download initiiert hat.

Es können nur die folgenden Digital Media-Formate heruntergeladen werden:

-   Advanced Systems Format (ASF)
-   MP3
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)

Der *SourceUrl* -Parameter unterstützt keine Unicode-codierten Zeichen folgen. Er muss auf gültigen Inhalt zeigen. Umleitungen werden nicht unterstützt.

Bei der Verwendung von Windows XP werden Audiodateien automatisch in die entsprechenden **eigenen Musik** -Unterordner auf der Grundlage von Metadatenwerten auf Dateiebene platziert. Video Dateien werden in \\ den Zufallszahlen-Typ für den Musik \\ Download eingefügt \\  \\ , wobei " *Random Number* " ein von Windows Media Player für jeden Benutzer generierter zufälliger Wert ist, und " *Type* " ist abhängig vom Downloadtyp entweder "Real Time" oder "Background".

Bei der Verwendung von Windows Media Player 9-Serie mit Windows 98 und Windows Millennium Edition (Me) werden Audiodateien und Videodateien in \\ den \\ \\ *Zufallszahlen*-Typ "Musikdownload" eingefügt \\ , wobei " *Random Number* " ein zufälliger Wert ist, der vom Player für jeden Benutzer generiert wird, und " *Type* " ist abhängig vom Downloadtyp entweder "Real Time" oder "Background".

Beachten Sie, dass Dateien möglicherweise auf der Grundlage der in der Datei enthaltenen Metadatenattribute und der vom Benutzer im Dialogfeld **Optionen** angegebenen Regeln umbenannt werden. Dateien, die keine Metadaten enthalten (z. b. **Album** oder **Artist**), werden möglicherweise in Ordner mit der Bezeichnung Unknown Artist oder Unknown Album verschoben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Collection-Objekt**](downloadcollection-object.md)
</dt> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





