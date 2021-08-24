---
description: Die IPropertySetter-Schnittstelle legt Eigenschaften für einen Effekt oder Übergang in DirectShow Editing Services (DES) fest. Um diese Schnittstelle zu verwenden, erstellen Sie eine Instanz eines Eigenschaftensetterobjekts (CLSID \_ PropertySetter) und ordnen sie einem Effekt oder Übergang zu, indem Sie die IAMTimelineObj::SetPropertySetter-Methode aufrufen. Weitere Informationen finden Sie unter Arbeiten mit Effekten und Übergängen. Normalerweise muss eine Anwendung nur die IPropertySetter::ClearProps-Methode aufrufen, um vorhandene Eigenschaften zu löschen, und die IPropertySetter::AddProp-Methode, um neue Eigenschaften hinzuzufügen. Die anderen Methoden auf dieser Schnittstelle werden von anderen DES-Komponenten aufgerufen.
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: IPropertySetter-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c6dc32c25c85893eeb2e9872bcf67be974489ec82fdd4d09c19a2341f6867ade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831030"
---
# <a name="ipropertysetter-interface"></a>IPropertySetter-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IPropertySetter` Schnittstelle legt Eigenschaften für einen Effekt oder Übergang in [DirectShow Editing Services](directshow-editing-services.md) (DES) fest.

Um diese Schnittstelle zu verwenden, erstellen Sie eine Instanz eines Eigenschaftensetterobjekts (CLSID \_ PropertySetter) und ordnen sie einem Effekt oder Übergang zu, indem Sie die [**IAMTimelineObj::SetPropertySetter-Methode**](iamtimelineobj-setpropertysetter.md) aufrufen. Weitere Informationen finden Sie unter [Arbeiten mit Effekten und Übergängen.](working-with-effects-and-transitions.md)

Normalerweise muss eine Anwendung nur die [**IPropertySetter::ClearProps-Methode**](ipropertysetter-clearprops.md) aufrufen, um vorhandene Eigenschaften zu löschen, und die [**IPropertySetter::AddProp-Methode,**](ipropertysetter-addprop.md) um neue Eigenschaften hinzuzufügen. Die anderen Methoden auf dieser Schnittstelle werden von anderen DES-Komponenten aufgerufen.

## <a name="members"></a>Member

Die **IPropertySetter-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPropertySetter** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IPropertySetter-Schnittstelle** verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Fügt dem Eigenschaftensetter eine Eigenschaft hinzu, wobei ein Array von Zeit-Wert-Paaren den Wert der Eigenschaft über einen Zeitraum definiert.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Löscht alle Eigenschaftendaten aus dem Eigenschaftensetter.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Klont einen Satz von Eigenschaften aus diesem Eigenschaftensetter und fügt sie einem neuen Eigenschaftensetter hinzu.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Gibt von der [**IPropertySetter::GetProps-Methode**](ipropertysetter-getprops.md) zugeordnete Ressourcen frei.<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Ruft die für dieses Objekt festgelegten Eigenschaften mit den entsprechenden Werten ab.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Lädt Eigenschaftsdaten aus einem Persistenzformat.<br/>                                                                                     |
| [**Loadxml**](ipropertysetter-loadxml.md)           | Lädt Eigenschaftsdaten, ausgedrückt in Extensible Markup Language (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Konvertiert Eigenschaftsdaten in eine XML-Zeichenfolge.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Speichert die Eigenschaftsdaten in einem Persistenzformat.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Legt die Eigenschaften des Zielobjekts auf den geeigneten Zustand für die angegebene Zeit fest.<br/>                                          |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
