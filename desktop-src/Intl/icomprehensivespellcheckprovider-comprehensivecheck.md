---
description: Überprüfen Sie den Anbietertext gründlicher als ISpellCheckProvider::Check.
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: IComprehensiveSpellCheckProvider::ComprehensiveCheck-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: ee1b07eb2f459aca3955b0a1c5ad2e2e2139cc196f618430b3039b1eba1e3971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086600"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>IComprehensiveSpellCheckProvider::ComprehensiveCheck-Methode

Überprüfen Sie den Anbietertext gründlicher als [**ISpellCheckProvider::Check.**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)

## <a name="syntax"></a>Syntax


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Text* \[ In\]
</dt> <dd>

Der zu überprüfende Text.

</dd> <dt>

*Ergebnis* \[ out\]
</dt> <dd>

Das Ergebnis der Überprüfung dieses Texts als Enumeration von Rechtschreibfehlern ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), falls vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabewert                                                                             | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>         | Erfolgreiche.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | *text* ist eine leere Zeichenfolge.<br/> |
| <dl> <dt>E \_ POINTER</dt> </dl>    | *text* ist ein NULL-Zeiger.<br/>  |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle muss nicht von einem Rechtschreibprüfungsanbieter implementiert werden. Wenn der Anbieter jedoch zwei "Modi" der Rechtschreibprüfung unterstützt (einen schnelleren und einen langsameren, aber gründlicheren), sollte er diese Schnittstelle in demselben Objekt implementieren, das [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) implementiert, um den gründlicheren Überprüfungsmodus zu unterstützen. Wenn ein Client [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)aufruft, ruft die Rechtschreibprüfungsfunktion [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) an den Anbieter für [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)und **IComprehensiveSpellCheckProvider.ComprehensiveCheck** auf, wenn die Schnittstelle unterstützt wird. Wenn die Schnittstelle nicht unterstützt wird, wird im Hintergrund auf [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)zurückverlegt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
