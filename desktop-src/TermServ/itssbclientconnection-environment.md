---
title: Itssbclientconnection-Umgebungs Eigenschaft
description: Ruft ein Objekt ab, das Informationen über die Umgebung enthält, die den Zielcomputer hostet.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Umgebungs Eigenschaften Remotedesktopdienste
- Umgebungs Eigenschaft Remotedesktopdienste, itssbclientconnection-Schnittstelle
- Itssbclientconnection-Schnittstelle Remotedesktopdienste, Umgebungs Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477724"
---
# <a name="itssbclientconnectionenvironment-property"></a>Itssbclientconnection:: Environment-Eigenschaft

Ruft ein Objekt ab, das Informationen über die Umgebung enthält, die den Zielcomputer hostet. In einem Szenario mit virtuellen Desktops würde dieses Objekt z. b. Informationen über den Computer enthalten, der die virtuelle Maschine hostet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen Zeiger auf ein [**itssbenvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) -Umgebungs Objekt.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Mögliche Werte sind u. a. die in der folgenden Liste aufgeführten Werte:

<dl> <dt>

E- \_ Zeiger
</dt> <dd>

Die Umgebung wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Orchestrierungs-Plug-in kann diese Methode aufrufen, um Umgebungs Informationen zu einem virtuellen Zielcomputer abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbclientconnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





