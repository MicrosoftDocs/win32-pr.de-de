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
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364758"
---
# <a name="extendedproperty-object"></a>ExtendedProperty-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Das **ExtendedProperty** -Objekt stellt eine von Microsoft erweiterte Eigenschaft dar.

## <a name="when-to-use"></a>Verwendung

Das **ExtendedProperty** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Legen Sie den Typ der erweiterten Eigenschaft fest, oder rufen Sie ihn ab.
-   Legt den Codierungstyp fest, der zum Codieren der erweiterten Eigenschaft verwendet wird, oder ruft diesen ab.

## <a name="members"></a>Member

Das **ExtendedProperty** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ExtendedProperty** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PROPID**](extendedproperty-propid.md)<br/> | Lesen/Schreiben<br/> | Ein Wert der [**CAPICOM \_ PROPID**](capicom-propid.md) -Enumeration, der den Typ der erweiterten Eigenschaft festlegt oder abruft.<br/> Dies ist die Standard Eigenschaft.<br/> |
| [**Wert**](extendedproperty-value.md)<br/>   | Lesen/Schreiben<br/> | Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, die die erweiterten Eigenschaften Daten festlegt oder abruft.<br/>                              |



 

## <a name="remarks"></a>Bemerkungen

Das **ExtendedProperty** -Objekt wird von der [**ExtendedProperties**](extendedproperties.md) -Auflistung verwendet.

Das **ExtendedProperty** -Objekt kann erstellt werden und ist für die Skripterstellung nicht sicher. Die ProgID für das **ExtendedProperty** -Objekt ist CAPICOM. ExtendedProperty. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
