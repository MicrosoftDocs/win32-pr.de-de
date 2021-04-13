---
description: Bietet Zugriff auf Kontext Objekteigenschaften, die sich auf Transaktionen beziehen.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Icontexttransaktioninfo-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483438"
---
# <a name="icontexttransactioninfo-interface"></a>Icontexttransaktioninfo-Schnittstelle

Bietet Zugriff auf Kontext Objekteigenschaften, die sich auf Transaktionen beziehen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie sollten diese Schnittstelle nicht implementieren. Die Standard Implementierung bietet umfassende Funktionen.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle für den Zugriff auf Kontext Objekteigenschaften, die sich auf Transaktionen beziehen.

## <a name="members"></a>Member

Die **icontexttransaktioninfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Icontexttransaktioninfo** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **icontexttransaktioninfo** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                         | BESCHREIBUNG                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Fetchtransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Ruft ggf. den Transaktions-oder Transaktions Proxy ab, der dem aktuellen Kontext zugeordnet ist.<br/>              |
| [**Gettxisolationlevelandtimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Ruft die Isolationsstufe und den Timeout Wert einer Transaktion ab, die im Stamm Transaktionskontext gehostet wird.<br/> |
| [**Registertransaktionproxy**](icontexttransactioninfo-fetchtransaction.md)                   | Ordnet eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung dem aktuellen Kontext zu.<br/>            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/> |



 

