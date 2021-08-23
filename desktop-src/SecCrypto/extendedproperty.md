---
description: Stellt eine von Microsoft erweiterte Eigenschaft dar.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927d35f73cec1f9e9032c326097a642349d6faa7e02d533330303016184a4bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007048"
---
# <a name="extendedproperty-object"></a>ExtendedProperty-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktion [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) auf aufruft und die Eigenschaften zu erhalten. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Das **ExtendedProperty-Objekt** stellt eine von Microsoft erweiterte Eigenschaft dar.

## <a name="when-to-use"></a>Verwendung

Das **ExtendedProperty-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Legen Sie den Typ der erweiterten Eigenschaft fest, oder rufen Sie diesen ab.
-   Legen Sie den Codierungstyp fest, der zum Codieren der erweiterten Eigenschaft verwendet wird, oder rufen Sie diesen ab.

## <a name="members"></a>Member

Das **ExtendedProperty-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ExtendedProperty-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp           | Beschreibung                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Lesen/Schreiben<br/> | Ein Wert der [**CAPICOM \_ PROPID-Enumeration,**](capicom-propid.md) der den Typ der erweiterten Eigenschaft fest legt oder abruft.<br/> Dies ist die Standardeigenschaft.<br/> |
| [**Wert**](extendedproperty-value.md)<br/>   | Lesen/Schreiben<br/> | Ein Wert der [**CAPICOM \_ ENCODING \_ TYPE-Enumeration,**](capicom-encoding-type.md) der die erweiterten Eigenschaftsdaten fest legt oder abruft.<br/>                              |



 

## <a name="remarks"></a>Hinweise

Das **ExtendedProperty-Objekt** wird von der [**ExtendedProperties-Auflistung**](extendedproperties.md) verwendet.

Das **ExtendedProperty-Objekt** kann erstellt werden, und es ist nicht sicher für Skripts. Die ProgID für das **ExtendedProperty-Objekt** ist CAPICOM. ExtendedProperty.1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
