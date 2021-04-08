---
title: v1_enum-Attribut
description: Das Attribut \ v1 \_ enum \ leitet, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standardwert übertragen wird.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum Attribut-Mittel l
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857439"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="51f60-104">v1-Aufzählungs \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="51f60-104">v1\_enum attribute</span></span>

<span data-ttu-id="51f60-105">Das Attribut **\[ v1 \_ Enumeration \]** leitet, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standardwert übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="51f60-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="51f60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51f60-106">Parameters</span></span>

<span data-ttu-id="51f60-107">Dieses Attribut hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="51f60-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f60-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51f60-108">Remarks</span></span>

<span data-ttu-id="51f60-109">Die Verwendung des **\[ v1 \_ \]** -Enumerationsattributs, um einen enumerierten Typ als 32-Bit-Entität zu übertragen, erhöht die Effizienz des Marshalling und entmarshalling von Daten, wenn eine solche Enumeration in Strukturen oder Unions eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="51f60-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="51f60-110">Um die Leistung zu verbessern, wird empfohlen, das **\[ v1- \_ \] Enumeration** -Attribut auf Enumeratoren in 32-Bit-Anwendungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="51f60-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="51f60-111">Beachten Sie jedoch, dass der C-Compiler auf 16-Bit-Plattformen einen enumerierten Typ als 16-Bit- [**int**](int.md)behandelt. Daher müssen für 16-Bit-Client Anwendungen [](enum.md) Enumerationstypen für die Remote Übertragung in [**Long**](long.md) konvertiert werden, um das Überschreiben von Daten oder das Senden falscher Werte zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="51f60-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="51f60-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51f60-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="51f60-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51f60-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f60-114">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="51f60-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="51f60-115">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="51f60-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="51f60-116">**lange**</span><span class="sxs-lookup"><span data-stu-id="51f60-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




