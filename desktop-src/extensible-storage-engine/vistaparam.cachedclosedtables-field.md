---
description: Weitere Informationen finden Sie im Feld "vistaparam. cachedclosedtables".
title: Vistaparam. cachedclosedtables-Feld (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128149"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="9ae03-103">Vistaparam. cachedclosedtables-Feld</span><span class="sxs-lookup"><span data-stu-id="9ae03-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="9ae03-104">Dieser Parameter steuert die Anzahl der B +-strukturressourcen, die von der-Instanz zwischengespeichert wurden, nachdem die Tabellen, die Sie darstellen, von der Anwendung geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="9ae03-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="9ae03-105">Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ae03-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="9ae03-106">Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</span><span class="sxs-lookup"><span data-stu-id="9ae03-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="9ae03-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ae03-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9ae03-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9ae03-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae03-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ae03-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="9ae03-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ae03-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ae03-111">Referenz</span><span class="sxs-lookup"><span data-stu-id="9ae03-111">Reference</span></span>

[<span data-ttu-id="9ae03-112">Vistaparam-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ae03-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="9ae03-113">Vistaparam-Member</span><span class="sxs-lookup"><span data-stu-id="9ae03-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="9ae03-114">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ae03-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
