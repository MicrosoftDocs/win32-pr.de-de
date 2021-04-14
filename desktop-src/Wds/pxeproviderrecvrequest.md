---
title: Pxeproviderrecvrequest-Rückruffunktion
description: Wird aufgerufen, wenn eine Anforderung von einem Client empfangen wird.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Pxeproviderrecvrequest-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391915"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>Pxeproviderrecvrequest-Rückruffunktion

Wird aufgerufen, wenn eine Anforderung von einem Client empfangen wird. Diese Funktion wird durch Aufrufen der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert, wobei der *CallbackType* -Parameter auf **PXE \_ Callback \_ recv \_ Request** festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hclientrequest* \[ in\]
</dt> <dd>

Handle für eine Anforderung, die von einem Client empfangen wurde.

</dd> <dt>

*ppacket* \[ in\]
</dt> <dd>

Zeiger auf den Arbeitsspeicher Puffer, der das empfangene Paket enthält.

</dd> <dt>

*upacketlen* \[ in\]
</dt> <dd>

Länge (in Byte) des Puffers, auf den der *ppacket* -Parameter verweist.

</dd> <dt>

*plocaladdress* \[ in\]
</dt> <dd>

Zeiger auf eine [**PXE- \_ Adress**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) Struktur, die die lokale Adresse enthält, an der das Paket empfangen wurde.

</dd> <dt>

*prämoteaddress* \[ in\]
</dt> <dd>

Zeiger auf eine [**PXE- \_ Adress**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) Struktur, die die Quelladresse des Pakets enthält.

</dd> <dt>

*pAction* \[ vorgenommen\]
</dt> <dd>

Gibt die Aktion an, die das System ausführen sollte.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt> </dl>                | Der Anbieter hat an einen Client mit einem Standard-DHCP-Antwortpaket geantwortet, das einen Pfad zum Netzwerkstart Programm enthält. Die Rückgabe dieser Aktion bedeutet, dass der Anbieter die Client Anforderung erfolgreich abgeschlossen hat, indem er die [**pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion mindestens einmal aufgerufen hat.<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <dt>**PXE \_ BA \_ Benutzer**</dt> definiert <dt>2</dt> </dl>       | Der Anbieter hat eine benutzerdefinierte Antwort an einen Client geantwortet, die nicht den DHCP-Spezifikationen entspricht. Die Rückgabe dieser Aktion bedeutet, dass der Anbieter die Client Anforderung erfolgreich abgeschlossen hat, indem er die [**pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion mindestens einmal aufgerufen hat.<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <dt>**PXE \_ BA \_ Ignore**</dt> <dt>3</dt> </dl>       | Der Anbieter möchte die Client Anforderung nicht bedienen, und die Anforderung sollte nicht an den nächsten Anbieter weitergeleitet werden. Alle Ressourcen, die der Client Anforderung zugeordnet sind, werden freigegeben, und die Client Anforderung wird ignoriert. Anbieter können diesen Wert auch verwenden, wenn Sie den Client erkennen, aber die Anforderung falsch formatiert war.<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <dt>**PXE \_ BA \_ abgelehnt**</dt> <dt>4</dt> </dl> | Der Anbieter möchte die Client Anforderung nicht bedienen. Das System übergibt die Anforderung an den nächsten Anbieter in der Liste der registrierten Anbieter. Wenn dies der letzte Anbieter in der Liste ist, werden alle der Client Anforderung zugeordneten Ressourcen freigegeben, und die Client Anforderung wird ignoriert.<br/>                     |



 

</dd> <dt>

*pContext* \[ in\]
</dt> <dd>

Der Kontextwert, der an die [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion übergeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Anbieter die Client Anforderung erfolgreich verarbeitet hat, sollte der Rückruf **Fehler \_** erfolgreich zurückgeben, und die **PXE- \_ Start \_ Aktion** , auf die der *pAction* -Parameter verweist, enthält die entsprechende Start Aktion für diese Anforderung. Wenn der Anbieter die Client Anforderung asynchron verarbeitet, sollte der Rückruf Fehler-e/a **\_ \_ Ausstehend** zurückgeben und die [**pxeasyncrecvdone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) -Funktion aufzurufen, wenn die Client Anforderung verarbeitet wurde. Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden, und das System wird so fortgesetzt, als ob die von **PXE \_ BA \_ Abgelehnte** Start Aktion angegeben wurde.

## <a name="remarks"></a>Bemerkungen

Der Typ von Paketen, die von einem Anbieter erkannt werden, kann mit der [**pxeprovidersetattribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) -Funktion geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Server Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-server-functions.md)
</dt> <dt>

[**Pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[**Pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**Pxeproviderationtattribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





