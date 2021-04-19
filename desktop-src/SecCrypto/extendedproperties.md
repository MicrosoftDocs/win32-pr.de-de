---
description: Stellt eine Auflistung von ExtendedProperty-Objekten dar.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: ExtendedProperties-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361968"
---
# <a name="extendedproperties-object"></a>ExtendedProperties-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Das **ExtendedProperties** -Objekt stellt eine Auflistung von [**ExtendedProperty**](extendedproperty.md) -Objekten dar. Jedes-Objekt stellt eine einzelne erweiterte Eigenschaft dar.

## <a name="when-to-use"></a>Verwendung

Das **ExtendedProperties** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Fügen Sie ein [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung hinzu, oder entfernen Sie es.
-   Ruft die Anzahl der erweiterten Eigenschaften in der Auflistung ab.
-   Rufen Sie ein bestimmtes [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **ExtendedProperties** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#extendedproperties-object)

### <a name="methods"></a>Methoden

Das **ExtendedProperties** -Objekt verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Eren**](extendedproperties-add.md)       | Fügt der Auflistung ein [**ExtendedProperty**](extendedproperty.md) -Objekt hinzu.<br/>      |
| [**Aufgeh**](extendedproperties-remove.md) | Entfernt ein [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **ExtendedProperties** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](extendedproperties-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](extendedproperties-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl von [**ExtendedProperty**](extendedproperty.md) -Objekten in der-Auflistung ab.<br/>                                                                                                                      |
| [**Element**](extendedproperties-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**ExtendedProperty**](extendedproperty.md) -Objekt ab, das die indizierte erweiterte Eigenschaft der Auflistung darstellt. Dies ist die Standard Eigenschaft.<br/>                                                      |



 

## <a name="remarks"></a>Bemerkungen

Das **ExtendedProperties** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
