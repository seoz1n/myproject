import streamlit as st

st.set_page_config(page_title="퍼스널 컬러 화장품 추천기", layout="centered")

st.title("💄 퍼스널 컬러 기반 화장품 추천기")

# Step 1: 퍼스널 컬러 선택
st.subheader("1. 퍼스널 컬러를 선택하세요")
personal_color = st.selectbox(
    "당신의 퍼스널 컬러는 무엇인가요?",
    ["봄웜", "여름쿨", "가을웜", "겨울쿨"]
)

# Step 2: 화장품 종류 선택
st.subheader("2. 화장품 종류를 선택하세요")
cosmetic_type = st.selectbox(
    "어떤 종류의 화장품을 찾고 계신가요?",
    ["립", "파운데이션", "아이섀도우", "블러셔", "마스카라"]
)

# 추천 결과 딕셔너리
recommendations = {
    "봄웜": {
        "립": ("3CE 립 컬러", "https://www.stylenanda.com/category/3ce-lip/2001/"),
        "파운데이션": ("에스쁘아 비 실크 파운데이션", "https://www.espoir.com/ko/pd/100112006"),
        "아이섀도우": ("클리오 프로 아이 팔레트 코랄", "https://www.cliocosmetic.com/ko/product/detail?productId=123"),
        "블러셔": ("페리페라 잉크 블러셔", "https://www.peripera.co.kr/ko/blush"),
        "마스카라": ("이니스프리 스키니 마스카라", "https://www.innisfree.com/kr/ko/product/productView.do?prdSeq=26161")
    },
    "여름쿨": {
        "립": ("롬앤 쥬시 래스팅 틴트 쿨톤 컬러", "https://romand.co.kr/product/list.html?cate_no=68"),
        "파운데이션": ("라네즈 네오 쿠션", "https://www.laneige.com/kr/ko/product/makeup/neo-cushion-matte.html"),
        "아이섀도우": ("에뛰드 플레이 컬러 아이즈 라벤더", "https://
