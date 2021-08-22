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
ms.openlocfilehash: 0225582217df56f486a44f12e3ca6ea0003130fdb209fb67e9f9e4ee258764d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007238"
---
# <a name="extendedproperties-object"></a>ExtendedProperties-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktion [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) auf aufruft und die Eigenschaften zu erhalten. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Das **ExtendedProperties-Objekt** stellt eine Auflistung von [**ExtendedProperty-Objekten**](extendedproperty.md) dar. Jedes -Objekt stellt eine einzelne erweiterte Eigenschaft dar.

## <a name="when-to-use"></a>Verwendung

Das **ExtendedProperties-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Hinzufügen oder Entfernen eines [**ExtendedProperty-Objekts**](extendedproperty.md) aus der Auflistung.
-   Ruft die Anzahl der erweiterten Eigenschaften in der Auflistung ab.
-   Ruft ein [**bestimmtes ExtendedProperty-Objekt**](extendedproperty.md) aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **ExtendedProperties-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#extendedproperties-object)

### <a name="methods"></a>Methoden

Das **ExtendedProperties-Objekt** verfügt über diese Methoden.



| Methode                                      | Beschreibung                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Hinzufügen**](extendedproperties-add.md)       | Fügt der [**Auflistung ein ExtendedProperty-Objekt**](extendedproperty.md) hinzu.<br/>      |
| [**Entfernen**](extendedproperties-remove.md) | Entfernt ein [**ExtendedProperty-Objekt**](extendedproperty.md) aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **ExtendedProperties-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | Beschreibung                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](extendedproperties-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**ExtendedProperty-Objekte**](extendedproperty.md) in der Auflistung ab.<br/>                                                                                                                      |
| [**Element**](extendedproperties-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**ExtendedProperty-Objekt**](extendedproperty.md) ab, das die indizierte erweiterte Eigenschaft der Auflistung darstellt. Dies ist die Standardeigenschaft.<br/>                                                      |



 

## <a name="remarks"></a>Hinweise

Das **ExtendedProperties-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
