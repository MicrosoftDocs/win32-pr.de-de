---
title: Datentyp Attribute
description: Sie können diese Attribute auf Datentypen in einer typedef-Anweisung anwenden, um die Verwendung oder den Effekt des Datentyps weiter zu definieren.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL-Mittell, Attribute, Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714369"
---
# <a name="data-type-attributes"></a><span data-ttu-id="a9ec1-104">Datentyp Attribute</span><span class="sxs-lookup"><span data-stu-id="a9ec1-104">Data Type Attributes</span></span>

<span data-ttu-id="a9ec1-105">Sie können diese Attribute auf Datentypen in einer [**typedef**](typedef.md) -Anweisung anwenden, um die Verwendung oder den Effekt des Datentyps weiter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="a9ec1-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="a9ec1-106">Attribute</span></span>                                 | <span data-ttu-id="a9ec1-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a9ec1-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9ec1-108">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="a9ec1-109">Identifiziert ein Bindungs handle, das Statusinformationen (Kontextinformationen) auf einem bestimmten Server zwischen Remote Prozedur Aufrufen von einem bestimmten Client verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="a9ec1-110">Nicht gültig für [**Objekt**](object.md) Schnittstellen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="a9ec1-111">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="a9ec1-112">Gibt einen spezifischen Handlertyp an, der für die Anwendung spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="a9ec1-113">**MS- \_ Union**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="a9ec1-114">Steuert die NDR-Ausrichtung von nicht gekapselten Unions.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="a9ec1-115">Verwenden Sie für die Verwendung von [**typedef**](typedef.md)s, um die Abwärtskompatibilität mit Schnittstellen zu verwenden, die mit der Mittell 2,0 1,0</span><span class="sxs-lookup"><span data-stu-id="a9ec1-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="a9ec1-116">**Kanal**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="a9ec1-117">Ermöglicht die Übertragung eines geöffneten Datenstroms für typisierte Daten über einen Remote Prozedur Aufruf.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="a9ec1-118">Ein [**in**](in.md) Pipe-Parameter ermöglicht dem Server das Abrufen des Datenstroms vom Client während eines Remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="a9ec1-119">Ein Out-Pipe-Parameter ermöglicht es dem Server, den Datenstrom an den Client zurück [**zusenden**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="a9ec1-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="a9ec1-120">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="a9ec1-121">Gibt an, wie ein Datentyp über ein Netzwerk übertragen wird, das für das benutzerdefinierte Marshalling verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="a9ec1-122">**v1-Aufzählung \_**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="a9ec1-123">Weist an, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standardwert übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="a9ec1-124">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="a9ec1-125">Ähnlich wie bei der über [**Tragung \_ als**](transmit-as.md) , aber implementieren Sie die Routinen, um die Daten zu verkleinern, zu Mars Hallen, zu entsperren und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 




