---
title: Imstscax-Methode der Methode "foratevirtualchannels"
description: Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste "der Methode" "," imstscax "-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "" der Methode "imsrdpclient"
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient2",-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient3",-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient4",-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient5",-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient6",-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient7",-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient8",-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient9",-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477733"
---
# <a name="imstscaxcreatevirtualchannels-method"></a>Imstscax:: foratevirtualchannels-Methode

Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Eine durch Trennzeichen getrennte Liste gültiger virtueller Channelnamen. Die Länge der einzelnen Namen in dieser Liste kann mindestens eins und maximal sieben alphabetischer Zeichen umfassen. Die Länge der gesamten Zeichenfolge kann mindestens eins und maximal 300 alphabetischer Zeichen umfassen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Gibt **E \_ invalidArg** zurück, wenn der übergebenen Parameter nicht die angegebenen Kriterien erfüllt.

## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Methode auf, bevor Sie die [**Connect**](imstscax-connect.md) -Methode aufrufen.

Informationen zu Benennungs Einschränkungen für virtuelle Kanäle finden Sie unter [Virtual Channel Client-Registrierung](virtual-channel-client-registration.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 





