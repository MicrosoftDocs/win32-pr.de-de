---
title: Extern. changeviewonlinelist-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. changeviewonlinelist-Methode
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- changeviewonlinelist-Methode, Windows Media Player
- changeviewonlinelist-Methode, Windows Media Player, externe Klasse
- Externe Klasse Windows Media Player, changeviewonlinelist-Methode
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358695"
---
# <a name="externalchangeviewonlinelist-method"></a>Extern. changeviewonlinelist-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **changeviewonlinelist** -Methode ändert die Ansicht in Windows Media Player, um eine Liste anzuzeigen, die dynamisch vom Online Store generiert wurde.

## <a name="syntax"></a>Syntax


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Librarylocationtype* \[ in\]
</dt> <dd>

Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ der neuen Ansicht angibt. Beispielsweise gibt die Konstante cpgenreid an, dass in der neuen Ansicht ein bestimmtes Genre angezeigt wird.

</dd> <dt>

*Librarylocationid* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die ID des bestimmten Elements enthält, das in der neuen Ansicht angezeigt werden soll. Wenn *librarylocationtype* beispielsweise cpgenreid ist, gibt dieser Parameter die ID des Genres an, das in der neuen Ansicht angezeigt werden soll. Diese Zeichenfolge kann leer sein.

</dd> <dt>

 Parameter \[ in\]
</dt> <dd>

**Zeichenfolge** , die Parameter enthält, die von Windows Media Player an das Plug-in des Online Stores durch Aufrufen von [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)weitergeleitet werden. Diese Parameter werden von Windows Media Player nicht interpretiert. Sie werden vom Online Shop erstellt und sind nur für den Online Shop von Bedeutung. Diese Zeichenfolge kann leer sein.

</dd> <dt>

*FriendlyName* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die einen anzeigen Amen enthält, der von Windows Media Player für die dynamische Liste angezeigt werden soll.

</dd> <dt>

*ListType* \[ in\]
</dt> <dd>

Eine Bibliotheks Speicherort Konstante, die den Typ der Elemente in der dynamisch generierten Liste angibt. Wenn der Wert dieses Parameters z. b. cptrackid ist, enthält die dynamische Liste die Spuren.

</dd> <dt>

*ViewMode* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Modus angibt, der von Windows Media Player verwendet wird, um die dynamische Liste anzuzeigen. Der Aufrufer muss diesen Parameter auf einen der folgenden Werte festlegen, die in "Contentpartner. h" definiert sind:

Viewmodereport

Viewmodedetails

Viewmodeicon

Viewmodetile

Viewmodeorderedlist

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Skript auf einer Ermittlungs Seite **changeviewonlinelist** aufruft, übergibt Windows Media Player einige Parameter an die [iwmpcontentpartner:: getlistcontent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) -Methode und die [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) -Methode, die vom Plug-in des Online Stores implementiert werden. In der folgenden Tabelle wird die Entsprechung zwischen den Parametern der drei Methoden gezeigt.



| changeviewonlinelist-Parameter | Getlistcontents-Parameter | GetTemplate-Parameter |
|--------------------------------|---------------------------|-----------------------|
| *LocationType*                 | *location*                | *location*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrinbiams*              | *bstrinviewparametriams*      |
| *Listentyp*                     | *bstrinlisttype*            | nicht zutreffend        |



 

Da alle drei Methoden in der obigen Tabelle durch den Online Shop implementiert werden, haben Sie bei der Verwendung der Parameter eine gewisse Flexibilität. Die Idee ist, dass Sie genügend Informationen für " **getlistcontent** " bereitstellen, um zu bestimmen, welche Liste abgerufen werden soll, und für " **GetTemplate** " zu ermitteln, welche Ermittlungs Seite als nächstes angezeigt werden soll In den folgenden Beispielen werden zwei Möglichkeiten veranschaulicht.

**Beispiel 1: eine dynamische Liste im Katalog des Online Stores**

Angenommen, Sie möchten, dass das Plug-in den Inhalt der dynamischen Liste mit der ID 6 im Katalog des Online Stores erhält. Angenommen, "List 6" ist eine Liste der Spuren. Sie können das Plug-in mit ausreichenden Informationen bereitstellen, indem Sie den folgenden-Befehl ausführen.


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



Beachten Sie, dass *der Parameter para* meters leer ist. das Plug-in verfügt über genügend Informationen in den anderen Parametern.

**Beispiel 2: eine dynamische Liste, die nicht im Katalog des Online Stores enthalten ist**

Angenommen, Sie möchten, dass das Plug-in den Inhalt einer dynamischen Liste erhält, die nicht im Katalog des Online Stores enthalten ist. Vielleicht haben Sie sich entschieden, eine dynamische Liste zu haben, die von einem bestimmten Künstler ausgewählte Lieder enthält. Angenommen, der Künstler hat eine ID von 2 im Katalog des Online Stores. Sie können den folgenden-Befehl ausführen.


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



Beachten Sie, dass die Parameter *LocationType* und *LocationID* die Liste nicht angeben. Stattdessen gibt der Parameter *para* meters die Liste an. Die Parameter *LocationType* und *LocationID* werden an **iwmpcontentpartner:: getlistcontent** übermittelt, in diesem Fall können Sie jedoch von **getlistcontent** ignoriert werden. Die *LocationType* -und *LocationID* -Parameter werden ebenfalls an **iwmpcontentpartner:: GetTemplate** übermittelt, die Sie verwenden können, um zu bestimmen, welche Ermittlungs Seite mit der dynamischen Liste angezeigt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Iwmpcontentpartner:: getlistcontents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**Iwmpcontentpartnercallback:: addlistcontents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**Iwmpcontentpartner:: GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





