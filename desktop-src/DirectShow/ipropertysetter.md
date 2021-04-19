---
description: 'Die ipropertysetter-Schnittstelle legt die Eigenschaften eines Effekts oder Übergangs in DirectShow-Bearbeitungs Diensten fest. Um diese Schnittstelle zu verwenden, erstellen Sie eine Instanz eines Eigenschaften Setter-Objekts (CLSID \_ propertysetter), und ordnen Sie es einem Effekt oder Übergang zu, indem Sie die iamtimelineobj:: setpropertysetter-Methode aufrufen. Weitere Informationen finden Sie unter Arbeiten mit Effekten und Übergängen. in der Regel muss eine Anwendung nur die ipropertysetter:: clearProperties-Methode aufrufen, um vorhandene Eigenschaften zu löschen, und die ipropertysetter:: addprop-Methode, um neue Eigenschaften hinzuzufügen. Die anderen Methoden für diese Schnittstelle werden von anderen des-Komponenten aufgerufen.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Ipropertysetter-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361990"
---
# <a name="ipropertysetter-interface"></a>Ipropertysetter-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IPropertySetter` Schnittstelle legt die Eigenschaften eines Effekts oder Übergangs in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fest.

Um diese Schnittstelle zu verwenden, erstellen Sie eine Instanz eines Eigenschaften Setter-Objekts (CLSID \_ propertysetter), und ordnen Sie es einem Effekt oder Übergang zu, indem Sie die [**iamtimelineobj:: setpropertysetter**](iamtimelineobj-setpropertysetter.md) -Methode aufrufen. Weitere Informationen finden Sie unter [Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md).

In der Regel muss eine Anwendung nur die [**ipropertysetter:: clearProperties**](ipropertysetter-clearprops.md) -Methode aufrufen, um vorhandene Eigenschaften zu löschen, und die [**ipropertysetter:: addprop**](ipropertysetter-addprop.md) -Methode, um neue Eigenschaften hinzuzufügen. Die anderen Methoden für diese Schnittstelle werden von anderen des-Komponenten aufgerufen.

## <a name="members"></a>Member

Die **ipropertysetter** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipropertysetter** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ipropertysetter** -Schnittstelle verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addprop**](ipropertysetter-addprop.md)           | Fügt dem Eigenschaften Setter eine Eigenschaft mit einem Array von Zeit-Wert-Paaren hinzu, das den Wert der Eigenschaft für einen Zeitraum definiert.<br/> |
| [**Clear-Eigenschaften**](ipropertysetter-clearprops.md)     | Löscht alle Eigenschaften Daten aus dem Eigenschaften Setter.<br/>                                                                                 |
| [**Clone-Eigenschaften**](ipropertysetter-cloneprops.md)     | Klont einen Satz von Eigenschaften aus diesem Eigenschaften Setter und fügt diese einem neuen Eigenschaften Setter hinzu.<br/>                                       |
| [**Freitext**](ipropertysetter-freeprops.md)       | Gibt Ressourcen frei, die von der [**ipropertysetter:: getrequiemethode**](ipropertysetter-getprops.md) zugeordnet werden.<br/>                             |
| [**Get-Eigenschaften**](ipropertysetter-getprops.md)         | Ruft die für dieses-Objekt festgelegten Eigenschaften mit den entsprechenden Werten ab.<br/>                                                      |
| [**Loadfromblob**](ipropertysetter-loadfromblob.md) | Lädt Eigenschaften Daten aus einem Persistenzformat.<br/>                                                                                     |
| [**LoadXml**](ipropertysetter-loadxml.md)           | Lädt Eigenschafts Daten, die in Extensible Markup Language (XML) ausgedrückt werden.<br/>                                                                 |
| [**Printxml**](ipropertysetter-printxml.md)         | Konvertiert Eigenschafts Daten in eine XML-Zeichenfolge.<br/>                                                                                         |
| [**Saveblob**](ipropertysetter-savetoblob.md)     | Speichert die Eigenschaften Daten in einem Persistenzformat.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Legt die Eigenschaften des Zielobjekts für den angegebenen Zeitraum auf den entsprechenden Zustand fest.<br/>                                          |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



 

 
