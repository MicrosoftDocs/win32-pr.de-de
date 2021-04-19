---
description: 'Überprüfen Sie den Anbieter Text auf eine gründlichere Weise als ispellcheckprovider:: Check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Icomprehensivespellcheckprovider:: comprehensivecheck-Methode'
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
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350176"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>Icomprehensivespellcheckprovider:: comprehensivecheck-Methode

Überprüfen Sie den Anbieter Text auf eine gründlichere Weise als [**ispellcheckprovider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Syntax


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Text* \[ in\]
</dt> <dd>

Der zu Überprüfung Ende Text.

</dd> <dt>

*Ergebnis* \[ vorgenommen\]
</dt> <dd>

Das Ergebnis der Überprüfung dieses Texts als eine Enumeration von Rechtschreibfehlern ([**ienumspellingerror**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), falls vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabewert                                                                             | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>         | Erfolgreich.<br/>                |
| <dl> <dt>E \_ invalidArg</dt> </dl> | *Text* ist eine leere Zeichenfolge.<br/> |
| <dl> <dt>E- \_ Zeiger</dt> </dl>    | *Text* ist ein NULL-Zeiger.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle muss nicht von einem Rechtschreib Prüfungs Anbieter implementiert werden. Wenn der Anbieter jedoch zwei "Modi" für die Rechtschreibprüfung unterstützt (eine schnellere und eine langsamere, aber gründlichere), sollte er diese Schnittstelle in demselben Objekt implementieren, das [**ispellcheckprovider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) implementiert, um den gründlicheren Überprüfungs Modus zu unterstützen. Wenn ein Client [**ispellchecker:: comprehensivecheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)aufruft, führt die Rechtschreibprüfungs Funktion den Anbieter für [**icomprehensivespellcheckprovider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider) [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aus und ruft **icomprehensivespellcheckprovider. verständsivecheck** auf, wenn die Schnittstelle unterstützt wird. Wenn die Schnittstelle nicht unterstützt wird, wird Sie automatisch auf [**ispellcheckprovider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)zurückgegriffen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icomprehensivespellcheckprovider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**Ienumspellingerror**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**Ispellchecker:: comprehensivecheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**Ispellcheckprovider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**Ispellcheckprovider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
