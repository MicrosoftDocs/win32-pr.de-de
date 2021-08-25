---
title: Eigenschaft "IMsTscNonScriptable ClearTextPassword"
description: Legt das Remotedesktop ActiveX-Steuerelementkennwort im Klartextformat fest.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- ClearTextPassword-Remotedesktopdienste
- ClearTextPassword-Eigenschaft Remotedesktopdienste , IMsTscNonScriptable-Schnittstelle
- IMsTscNonScriptable-Schnittstelle Remotedesktopdienste, ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable-Schnittstelle
- IMsRdpClientNonScriptable-Schnittstelle Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste , ClearTextPassword-Eigenschaft
- ClearTextPassword-Eigenschaft Remotedesktopdienste , MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste , ClearTextPassword-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0519e7379eab529cc5275c85a11116764417d524a03dff2e1eab74a914b6560b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125050"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>IMsTscNonScriptable::ClearTextPassword (Eigenschaft)

Legt das Remotedesktop ActiveX-Steuerelementkennwort im Klartextformat fest.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Eigenschaftswert

Das Kennwort, das zum Herstellen einer Verbindung verwendet werden soll, angegeben im Klartextformat.

## <a name="error-codes"></a>Fehlercodes

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Das Kennwort wird im sicher verschlüsselten RDP-Kommunikationskanal an den Server übergeben. Nachdem ein Klartextkennwort festgelegt wurde, kann es nicht mehr im Klartextformat abgerufen werden.

Die **ClearTextPassword-Eigenschaft** kann nur festgelegt werden, wenn sich Remotedesktop ActiveX Steuerelement nicht im verbundenen Zustand befindet. Das Festlegen dieser Eigenschaft schlägt fehl, wenn das Steuerelement verbunden ist. Um den verbundenen Zustand zu überprüfen, rufen Sie die [**IMsTscAx::Connected-Eigenschaft**](imstscax-connected.md) ab.

Sie können diese Methode auch aufrufen, um ein Klartextkennwort festzusetzen, bevor Sie es entweder in ein portierbares codiertes Kennwort oder in ein binäres (nicht portierbares) codiertes Kennwort konvertieren. Beachten Sie jedoch, dass codierte Kennwörter nicht als sicher verschlüsselt betrachtet werden sollten.

Wenn Sie diese Methode zuerst aufrufen, um ein Kennwort im Klartextformat festlegen, können Sie das Kennwort in ein codiertes Format konvertieren.

**So konvertieren Sie ein Klartextkennwort in ein codiertes Format**

1.  Legen Sie das Kennwort in der **ClearTextPassword-Eigenschaft im Klartextformat** fest.
2.  Um das Kennwort im binären (nicht portierbaren) codierten Format abzurufen, rufen Sie die [**BinaryPassword-Eigenschaft**](imstscnonscriptable-binarypassword.md) und die [**BinarySalt-Eigenschaften**](imstscnonscriptable-binarysalt.md) ab. Sowohl der codierte Kennwortteil als auch der Salt-Teil sind erforderlich, um ein Kennwort im binär codierten Format festlegen zu können.
3.  Rufen Sie zum Abrufen des Kennworts im portierbaren codierten Format die [**PortablePassword-Methode**](imstscnonscriptable-portablepassword.md) und die [**PortableSalt-Eigenschaften**](imstscnonscriptable-portablesalt.md) ab. Beide Teile sind erforderlich, um ein Kennwort im portierbaren codierten Format festlegen zu können.

Nach dem Ausführen der vorherigen drei Schritte können Sie das Kennwort im codierten Format festlegen, indem Sie die [**Eigenschaften BinaryPassword**](imstscnonscriptable-binarypassword.md) und [**BinarySalt**](imstscnonscriptable-binarysalt.md) oder [**PortablePassword**](imstscnonscriptable-portablepassword.md) und [**PortableSalt**](imstscnonscriptable-portablesalt.md) festlegen. Beide Teile sind erforderlich.

Um die automatische Anmeldung zu aktivieren, müssen Sie auch die [**Eigenschaften UserName und**](imstscax-username.md) [**Domain**](imstscax-domain.md) festlegen. Wenn das Kennwort den Benutzer nicht authentifizieren kann, wird das Dialogfeld Windows Anmeldung auf dem Server angezeigt, um den Benutzer zur Eingabe des Kennworts aufzugeben.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





