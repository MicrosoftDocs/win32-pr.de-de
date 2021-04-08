---
title: Imstscnonscriptable cleartextpassword (Eigenschaft)
description: Legt das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format fest.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Cleartextpassword-Eigenschaft Remotedesktopdienste
- Cleartextpassword-Eigenschaft Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
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
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743528"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Imstscnonscriptable:: cleartextpassword-Eigenschaft

Legt das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format fest.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Eigenschaftswert

Das Kennwort, das zum Herstellen der Verbindung verwendet werden soll, angegeben im nur-Text-Format.

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Das Kennwort wird im sicheren verschlüsselten RDP-Kommunikationskanal an den Server übermittelt. Nachdem ein Klartext-Kennwort festgelegt wurde, kann es nicht im nur-Text-Format abgerufen werden.

Die **cleartextpassword** -Eigenschaft kann nur festgelegt werden, wenn sich das Remotedesktop ActiveX-Steuerelement nicht im verbundenen Zustand befindet. Das Festlegen dieser Eigenschaft schlägt fehl, wenn das Steuerelement verbunden ist. Zum Überprüfen des verbundenen Zustands rufen Sie die [**imstscax:: Connected**](imstscax-connected.md) -Eigenschaft ab.

Sie können diese Methode auch aufrufen, um ein nur-Text-Kennwort festzulegen, bevor Sie es in ein portables codiertes Kennwort oder ein binäres (nicht Portables) codiertes Kennwort umwandelt. Beachten Sie jedoch, dass codierte Kenn Wörter nicht als sicher verschlüsselt angesehen werden sollten.

Wenn Sie diese Methode zum ersten Mal aufrufen, um ein Kennwort im nur-Text-Format festzulegen, können Sie das Kennwort in ein codiertes Format konvertieren.

**So konvertieren Sie ein Klartext-Kennwort in ein codiertes Format**

1.  Legen Sie das Kennwort im Klartext-Format in der **cleartextpassword** -Eigenschaft fest.
2.  Rufen Sie die Eigenschaft [**binarypassword**](imstscnonscriptable-binarypassword.md) und die Eigenschaften [**binarysalt**](imstscnonscriptable-binarysalt.md) ab, um das Kennwort im Binärformat (nicht portabel) abzurufen. Sowohl das codierte Kennwort als auch der Salt-Teil sind erforderlich, um ein Kennwort im Binärformat festzulegen.
3.  Rufen Sie die [**portablepassword**](imstscnonscriptable-portablepassword.md) -Methode und die [**portablesalt**](imstscnonscriptable-portablesalt.md) -Eigenschaften ab, um das Kennwort im portablen codierten Format abzurufen. Beide Teile sind erforderlich, um ein Kennwort im portablen codierten Format festzulegen.

Nachdem Sie die vorangegangenen drei Schritte ausgeführt haben, können Sie das Kennwort im codierten Format festlegen, indem Sie die Eigenschaften [**binarypassword**](imstscnonscriptable-binarypassword.md) und [**binarysalt**](imstscnonscriptable-binarysalt.md) oder [**portablepassword**](imstscnonscriptable-portablepassword.md) und [**portablesalt**](imstscnonscriptable-portablesalt.md) festlegen. Beide Teile sind erforderlich.

Um die automatische Anmeldung zu aktivieren, müssen Sie auch den [**Benutzernamen**](imstscax-username.md) und die [**Domänen**](imstscax-domain.md) Eigenschaften festlegen. Wenn das Kennwort den Benutzer nicht authentifizieren kann, wird das Dialogfeld Windows-Anmeldung auf dem Server angezeigt, um den Benutzer zur Eingabe des Kennworts aufzufordern.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





