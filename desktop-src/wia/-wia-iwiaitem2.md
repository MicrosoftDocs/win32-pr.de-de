---
description: Die IWiaItem2-Schnittstelle bietet Anwendungen die gleiche Funktionalität wie die iwiaitem-Schnittstelle (die Möglichkeit zum Abfragen von Geräten, um ihre Funktionen zu ermitteln, auf Datenübertragungs Schnittstellen und Element Eigenschaften zuzugreifen und das Gerät zu steuern).
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: IWiaItem2-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862679"
---
# <a name="iwiaitem2-interface"></a>IWiaItem2-Schnittstelle

Die **IWiaItem2** -Schnittstelle bietet Anwendungen die gleiche Funktionalität wie die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle (die Möglichkeit zum Abfragen von Geräten, um ihre Funktionen zu ermitteln, auf Datenübertragungs Schnittstellen und Element Eigenschaften zuzugreifen und das Gerät zu steuern). Außerdem bietet die Anwendung die Möglichkeit, Bild Verarbeitungs Filter dynamisch zu erstellen und zu verwenden, die als Erweiterungen der Windows-Abbild Erfassung (WIA) 2,0-Gerätetreiber in Windows Vista bereitgestellt werden können.

## <a name="members"></a>Member

Die **IWiaItem2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IWiaItem2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaItem2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Check Extension**](-wia-iwiaitem2-checkextension.md)                 | Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) -Methode verwendet werden kann. <br/>                                   |
| [**"Kreatechilditem"**](-wia-iwiaitem2-createchilditem.md)               | Erstellen Sie ein neues untergeordnetes Element. Fügt der **IWiaItem2** -Struktur eines Geräts **IWiaItem2** -Objekte hinzu. <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | Entfernt das aktuelle **IWiaItem2** -Objekt aus der Objektstruktur des Geräts. <br/>                                                                                                                          |
| [**Devicecommand**](-wia-iwiaitem2-devicecommand.md)                   | Gibt einen Befehl an ein WIA 2,0-Hardware Gerät aus. <br/>                                                                                                                                                   |
| [**Geräte-/vicedlg**](-wia-iwiaitem2-devicedlg.md)                           | Zeigt dem Benutzer ein Dialogfeld an, in dem die Bild Erfassung vorbereitet werden soll. <br/>                                                                                                                              |
| [**Diagnostics**](-wia-iwiaitem2-diagnostic.md)                         | Wird derzeit nicht unterstützt.<br/>                                                                                                                                                                          |
| [**Enumchilditems**](-wia-iwiaitem2-enumchilditems.md)                 | Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle für Ordner mit Elementen in der **IWiaItem2** -Struktur eines WIA 2,0-Geräts. <br/>        |
| [**Enumdävicecapabilitäten**](-wia-iwiaitem2-enumdevicecapabilities.md) | Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein WIA 2,0-Gerät unterstützt. <br/>                                                                                               |
| [**Enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | Die [**IWiaItem2:: enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) -Methode erstellt einen Enumerator, der zum Abrufen von Informationen über Ereignisse verwendet wird, für die eine Anwendung registriert ist.<br/> |
| [**Finditembyname**](-wia-iwiaitem2-finditembyname.md)                 | Durchsucht die Baumstruktur eines Elements anhand des Namens als Suchschlüssel. <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | Ruft die Erweiterungs Schnittstellen ab, die möglicherweise mit einem WIA 2,0-Gerätetreiber geliefert werden. <br/>                                                                                                                      |
| [**Getitemcategory**](-wia-iwiaitem2-getitemcategory.md)               | Ruft die Kategorieinformationen eines Elements ab. <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | Ruft Typinformationen eines Elements ab. <br/>                                                                                                                                                                 |
| [**Getparameentitem**](-wia-iwiaitem2-getparentitem.md)                   | Ruft das übergeordnete Element in der-Struktur ab, das ein WIA 2,0-Hardware Gerät darstellt. <br/>                                                                                                                      |
| [**Getpreviewcomponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | Ruft die WIA 2,0-Vorschau Komponente ab.<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | Ruft das Stamm Element einer Struktur von Item-Objekten ab, die zur Darstellung eines WIA 2,0-Hardware Geräts verwendet werden. <br/>                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Die WIA 2,0-Elementstruktur, die eine Anwendung sehen kann, ist getrennt von der Struktur, die von einem WIA 2,0 Minidriver erstellt und verwaltet wird. Wenn ein Mini Treiber eine Struktur von Elementen erstellt, verwendet der WIA 2,0-Dienst diese WIA-2,0-Elementstruktur als Leitfaden, um identische Kopien zu erstellen, die von Abbild Erstellungs Anwendungen angezeigt werden können. Elemente in der kopierten Struktur werden als Anwendungs Elemente bezeichnet. Elemente in der Struktur, die von einem Mini Treiber erstellt werden, werden als Treiber Elemente bezeichnet. In Windows Vista werden die WIA 2,0-Element Strukturen aus **IWiaItem2** -Objekten erstellt, von denen jedes die **IWiaItem2** -Schnittstelle implementiert).

Die **IWiaItem2** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
