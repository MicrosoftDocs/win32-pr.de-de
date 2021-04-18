---
description: 'Ruft den Namen des Zertifikats ab, das sich aus einem früheren erfolgreichen Aufrufen von "iscrdenr:: Enroll" ergibt.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Iscrdenr:: getenrolledcertifitorename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351426"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>Iscrdenr:: getenrolledcertifitorename-Methode

Die **getenrolledcertifitorename** -Methode ruft den Namen des Zertifikats ab, das sich aus einem früheren erfolgreichen Aufrufen von [**iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))ergibt.

Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen. Diese Methode ruft die [*CryptoAPI*](../secgloss/c-gly.md) -Funktion [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob das Zertifikat in einem Dialogfeld angezeigt wird. Wenn dieser Wert "SCard \_ ENROLL \_ No \_ Display \_ CERT (als 0x01 definiert)" lautet, wird das registrierte Zertifikat nicht angezeigt. alle anderen Werte bewirken, dass das registrierte Zertifikat im Dialogfeld " **Zertifikat** " angezeigt wird.

</dd> <dt>

*pbstraucertname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den abgerufenen Zertifikats Namen zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den abgerufenen Zertifikats Namen darstellt.

## <a name="remarks"></a>Bemerkungen

Da diese Methode für ein vorhandenes Zertifikat funktioniert, müssen Sie [**iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) erfolgreich aufrufen, bevor Sie **getenrolledcertifikatename** aufrufen können.

Die **getenrolledcertifitorename** -Methode ruft die [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) -Funktion auf, um den Zertifikat Namen entsprechend der für den "CERT \_ Name \_ Simple \_ Display Type" \_ -Wert des *dwType* -Parameters von **certgetnamestring** beschriebenen Sequenz abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscrdenr**](iscrdenr.md)
</dt> <dt>

[**Iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
