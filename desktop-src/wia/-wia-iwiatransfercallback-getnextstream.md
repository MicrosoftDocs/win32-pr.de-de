---
description: Ruft einen neuen Stream für das angegebene Element ab.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Iwiatransfercallback:: getnextstream-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356776"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a>Iwiatransfercallback:: getnextstream-Methode

Ruft einen neuen Stream für das angegebene Element ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstritemname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen des Elements an, für das der Stream erstellt werden soll.

</dd> <dt>

*bstraufullitemname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den vollständigen Namen des Elements an, für das der Stream erstellt werden soll.

</dd> <dt>

*ppdestination* \[ vorgenommen\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***

Empfängt die Adresse eines Zeigers auf das neue [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode von einem Bild Verarbeitungs Filter implementiert wird, ruft der Windows-Abbild Erfassungs Dienst (WIA) 2,0 Mini Treiber ihn während der Abbild Erfassung auf, um den Zielstream vom Client zu erhalten.

**Iwiatransfercallback:: getnextstream** eines Filters muss an die Rückruf Methode der Anwendung delegieren. Der Filter verwendet den Datenstrom, der von der **iwiatransfercallback:: getnextstream** -Implementierung des Anwendungs Rückrufs zurückgegeben wurde, um einen eigenen Stream zu erstellen, der an den WIA 2,0-Dienst zurückgegeben wird. Die Filterung erfolgt, wenn der Datenstrom des Filters die [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) -Methode aufruft.

Der Stream des Filters kann keine Annahmen über die Anzahl der Bytes machen, die bei jedem Schreibvorgang in ihn geschrieben werden, da die ungefilterten Image Daten möglicherweise von der WIA 2,0-Vorschau Komponente und nicht vom Treiber stammen. Die WIA 2,0-Vorschau Komponente schreibt die gesamten ungefilterten Bild Daten immer nur einmal in den Stream des Filters, was bedeutet, dass der Stream des Filters eine Quelle in Sie schreibt. Wenn sowohl der Treiber als auch die Vorschau Komponente in den Datenstrom des Filters schreiben, kann der streamingstream nicht davon ausgehen, dass er den vollständigen Header erhält, wenn [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) das erste Mal aufgerufen wird, obwohl der entsprechende Treiber immer zuerst die Header Daten in einem Schreibvorgang schreibt. Es kann auch nicht davon ausgegangen werden, dass ein nachfolgender Schreibvorgang genau eine Scan Zeile enthält. Der Filterungs Datenstrom muss also möglicherweise die Anzahl der zu schreibenden Bytes zählen, um z. b. zu ermitteln, wo die Bilddaten gestartet werden.

Die **iwiatransfercallback:: getnextstream** -Implementierung des Bild Verarbeitungs Filters sollte die Eigenschaften lesen, die für die Bildverarbeitung von dem Element benötigt werden, für das das Image abgerufen wird. Der Filter liest die Eigenschaften nicht direkt aus dem *pWiaItem2* , der in [**initializefilter**](-wia-iwiaimagefilter-initializefilter.md)übertragen wird. Stattdessen muss der Filter [**finditembyname**](-wia-iwiaitem2-finditembyname.md) für dieses WIA 2,0-Element aufrufen, um das tatsächliche WIA 2,0-Element abzurufen. Der Grund hierfür ist, dass das abgerufene Image tatsächlich ein untergeordnetes Element von *pWiaItem2* sein kann. Beispielsweise verwendet der Filter während einer Ordner Erfassung *pWiaItem2* , um die untergeordneten Elemente von *pWiaItem2* in **iwiatransfercallback:: getnextstream** abzurufen (während der Ordner Erfassung gibt der Treiber die Bilder zurück, die von den untergeordneten Elementen von *pWiaItem2* dargestellt werden). Dasselbe gilt, wenn die WIA 2,0-Vorschau Komponente den Bild Verarbeitungs Filter aufruft, indem ein untergeordnetes WIA 2,0-Element übergeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
